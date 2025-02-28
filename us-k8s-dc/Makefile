install:
	openvpn3 config-import \
		--config mx-UDP4-1197-config.ovpn \
		--persistent \
		--name us-akvelon
	openvpn3 config-manage \
		--config us-akvelon \
		--allow-compression yes
		
remove:
	openvpn3 config-remove \
		--config us-akvelon \
		--force

connect:
	make disconnect
	openvpn3 session-start \
		--config us-akvelon

disconnect:
	openvpn3 session-manage \
		--disconnect \
		--config us-akvelon || true

list:
	openvpn3 configs-list --verbose