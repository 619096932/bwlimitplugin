1���ù����ɲ��ʵ�֣������Ҫʵ���ɷ������˵��ͻ��˵��������٣�ʵ�ʹ��������������������㹻������Ҫ�������٣��ͻ��˵����д����Ǻܵ͵ģ���

2��������øù��ܣ���Ҫ���������ļ���vpn1.conf������������У������еĲ���Ϊ����������ļ�·����

plugin /usr/local/openvpn-2.2.3/lib/bwlimitplugin.so "/usr/local/openvpn-2.2.3/etc/bwlimitplugin.cnf"


3����Ҫ�޸Ĳ����Ͳ���������ļ�����������·��Ϊ��/usr/local/openvpn-2.2.3/etc/bwlimitplugin.cnf���������ʵ�����£�

[root@VPN-server-Xen etc]# cat bwlimitplugin.cnf 

#this is the config file for bwlimitplugin.so

#default  means all other clients whose cname not specified in the followed list

default 2048

#config the total rate for tun,which unit is mbps 
total   1000

#bw limit list
#user cname  bw(kbps)

user abc      100
user xyz      1000
user test      1560
user test1     1234

˵�������ٵ�������Ҫ���������֣��ܴ���ָ���û����ٴ���Ĭ���û����ٴ���
total�ؼ��ֺ������������   �����������ܴ�����λΪMbps��Ĭ��Ϊ100��ǧ������ͨ������Ϊ1000����
default�ؼ��ֺ������������  δ����ָ�����û������д�����λΪKbps��Ĭ��Ϊ2048Kbps����
user�ؼ��ֺ�����û����͸��û��Ĵ�������������ָ����4���û��������û���Ϊ��abc���û�����Ϊ100Kbps��