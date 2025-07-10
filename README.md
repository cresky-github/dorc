# dorc

修改成合适的 路径 

file_loc="/etc/smartdns/data/domain2loc.$Query_ID.csv"

file_noip="/etc/smartdns/data/noip.$Query_ID.txt"

file_loc="/etc/smartdns/data/domain2loc.csv"

file_noip="/etc/smartdns/data/noip.txt"
    
这是域名库的路径

dig +tcp +short $Domain -4 -p 5353 | sort -u -o $file_ipset_cn &

-p 5353 改成国内DNS（IP或端口）

dig +tcp +short $Domain -4 -p 5354 | sort -u -o $file_ipset_ncn &

-p 5353 改成国外DNS（IP或端口）

用到其它组件

[cide-merger] (https://github.com/zhanhb/cidr-merger)

