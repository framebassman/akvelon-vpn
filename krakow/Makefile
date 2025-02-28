install:
	openvpn config-import \
		--config krakow-UDP4-7793-dmitry.romashov-config.ovpn \
		--name pl-akvelon
		
remove:
	openvpn config-remove \
		--config pl-akvelon \
		--force

connect:
	make otp
	sudo openvpn \
		--config krakow-UDP4-7793-dmitry.romashov-config.ovpn

list:
	openvpn3 configs-list --verbose
	
otp:
	@read -p "Enter OTP:" otp; \
	echo "dmitry.romashov\n6730$$otp" > login.txt