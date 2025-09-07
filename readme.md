# Guide VPN Client Configure on .ovpn
export via mikrotik

```
client
dev tun
remote 103.x.x.x 1194 tcp <= ip public sever ovpn
tls-client
nobind
user nobody
group nogroup
persist-tun
persist-key
cipher AES-256-CBC
auth SHA512
verb 3
auth-user-pass
remote-cert-tls server

# redirect-gateway def1 <= klo lo mau smua trafik internet lewat vpn ini bisa aktifkan
route-nopull <= ini splite tunnel, akses server internet pake isp sendiri, dan akses server kantor pake vpn

# add subnet kantor biar bisa ngobrol sama jaringan local
route 192.168.0.0 255.255.255.0



<ca>
-----BEGIN CERTIFICATE-----
........
-----END CERTIFICATE-----
</ca>
<cert>
-----BEGIN CERTIFICATE-----
.......
-----END CERTIFICATE-----
</cert>
<key>
-----BEGIN ENCRYPTED PRIVATE KEY-----
.......
-----END ENCRYPTED PRIVATE KEY-----
</key>

```
