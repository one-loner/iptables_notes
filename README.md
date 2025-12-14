# IPTABLES NOTES
Just my private notes for iptables   
   
## Forwarding to transparent proxy    
### For sime user   
```bash
/usr/sbin/iptables -t nat -A OUTPUT -p tcp -m owner --uid-owner <USER_ID> -j REDIRECT --to-ports <Port of transparent proxy on localhost>
```\`
    
### For destenation IP
```bash
/usr/sbin/iptables -t nat -A OUTPUT -p tcp -d <IP> -j REDIRECT --to-ports <Port of transparent proxy on localhost>
```\`


