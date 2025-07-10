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


列说明

![image](https://github.com/user-attachments/assets/4a0a8d39-a391-4324-b3ae-0b4c99210ce2)

![image](https://github.com/user-attachments/assets/9f547a78-3334-46e7-9235-48bf0075fd82)

第一列，空

第二列，域名

第三列，国外DNS返回IP定位的地区

第四列，国外DNS返回IP

第五列，国内DNS返回IP定位的地区

第六列，国内DNS返回IP

第七列，COMM/DIRECT/PROXY 

    COMM 表示 国内/国外DNS解析结果相同（可以理解成没遭到染污）
    
    DIRECT 仅国内DNS解析返回值
    
    PROXY 仅国外DNS解析返回值
    
用到其它组件

[cide-merger] (https://github.com/zhanhb/cidr-merger)

