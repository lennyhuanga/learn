�γ̴��

1����������а�װCentOS
2����ÿ��CentOS�ж���װJava��Perl
3����4��������а�װCentOS��Ⱥ
4������4̨CentOSΪssh�����뻥��ͨ��

���㿪ʼ�����ֹ���һ��һ�����һ��4���ڵ��CentOS��Ⱥ

Ϊ���Ǻ���Ŀγ���׼��������ὲ����͵ķֲ�ʽ��redis��Ⱥ�ܹ���һ��һ�����ֹ��redis��Ⱥ����Ⱥ�������Ӽܹ����ֲ�ʽ��Ⱥ�ܹ�

���Ǻ���Ŀγ̣��ὲ��һЩʵʱ���㼼����Ӧ�ã�����storm������һ��storm�Ļ���֪ʶ������java����ʦ��˵�����þͿ����ˣ���һЩstorm������ķֲ�ʽʵʱ�����feature��ok�ˣ��һ��storm�ļ�Ⱥ

�����������׵�ϵͳ��nginx��tomcat+java webӦ�ã�mysql

��������ʵ���������˵Ļ�����ȥ�������ʾһ������ϵͳ�Ĳ��𣬲�Ҫ���ж�����redis��Ⱥ+storm��Ⱥ+nginx+tomcat+mysql��ȫ������һ���ڵ��������Ҳ����ȥ��һ�ԣ�������Ϊ�γ���˵��Ч������̫����

redis��Ⱥ��������һ�׻���
storm��Ⱥ��������һ�׻���
nginx����������
tomcat + java webӦ�ã���������
mysql����������

ʮ����������ȥ��������ϵͳ�������Լ��ıʼǱ������������εģ���ô����Ų�ס��

i5��12G

4̨�������ÿ̨�������1G���ڴ棬���Ի������ܳ�ס

���Ա�����6��G�ڴ�Ļ���ѧϰ���ִ��͵�ϵͳ�ܹ��Ŀγ̣����е����������ҽ��飬����G���ڴ�����Ҳ�ͼ��ٿ�Ǯ�����Լ���üӸ��ڴ��������ٵ�8G����

16G�պ�

���ֹ������㿪ʼ

�ܶ���Ƶ�γ̣����潲ʦ�����ֳɵ���������Լ���װ���ˣ��������ֱ�Ҫ������

���ε�ʱ��ֱ�ӻ����Լ���������Ϳ�ʼ������

�ܶ�ͬѧ�ͻᷢ�֣���Ҫ��������ʦһ���Ļ��������ѣ��Լ�������������װ�˸����������Ƿ��֣��������⣬���ֱ�������������

ѧϰ�γ̵Ĺ��̺ܼ���

ѧ��Ƶ�γ̣��϶���Ҫ������Ƶ�����еĶ����Լ�ȥ��һ������һ���������ȴ��Ϊ�������⣬�����ˣ������ˣ��Ǿ�̫����

��centos�ľ����ļ��������е���Ҫʹ�õ�������ȫ�����㣬���Լ������ϣ�����һ�����������������virtual box���Ϳ��Ը��������

�����һ��һ��������Ƶ�����������������Ӧ�����ⲻ��

�������⣬�����Ū��ɵ��ʽ��

------------------------------------------------------------------------------------------

1����������а�װCentOS

����һ��virtual box���������������vmware������Щ�꣬���ֲ�̫�ȶ�����Ҫ�ǵ�ʱ�һ��hadoop�����ݵļ�Ⱥ������ÿ�������Ժ�����������Ⱥ�͹ҵ��ˣ�

virtual box�����ֺ��ȶ�����Ⱥ������������ҹң����Ծ�һֱ��virtual box��

��1��ʹ�ÿγ��ṩ��CentOS 6.5���񼴿ɣ�CentOS-6.5-i386-minimal.iso��
��2���������������Virtual Box��������½�����ť���������һ�������������������Ϊeshop-cache01��ѡ�����ϵͳΪLinux��ѡ��汾ΪRed Hat������1024MB�ڴ棬�����ѡ��ȫ����Ĭ�ϣ���Virtual Disk File location and size�У�һ��Ҫ�Լ�ѡ��һ��Ŀ¼�����������ļ����������create����ť����ʼ�����������
��3�����������������ѡ�񴴽��õ����������������á���ť��������һ���У����ӷ�ʽ�У�ѡ��Bridged Adapter����
��4����װ������е�CentOS 6.5����ϵͳ��ѡ�񴴽��õ���������������ʼ����ť��ѡ��װ���ʣ������ص�CentOS 6.5�����ļ�����ѡ���һ�ʼ��װ-Skip-��ӭ����Next-ѡ��Ĭ������-Baisc Storage Devices-Yes, discard any data-������:spark2upgrade01-ѡ��ʱ��-���ó�ʼ����Ϊhadoop-Replace Existing Linux System-Write changes to disk-CentOS 6.5�Լ���ʼ��װ��
��5����װ���Ժ�CentOS��������Ҫ����һ�£�����reboot�����reboot�Ϳ����ˡ�

��6����������

vi /etc/sysconfig/network-scripts/ifcfg-eth0

DEVICE=eth0
TYPE=Ethernet
ONBOOT=yes
BOOTPROTO=dhcp
service network restart
ifconfig

BOOTPROTO=static
IPADDR=192.168.0.X
NETMASK=255.255.255.0
GATEWAY=192.168.0.1
service network restart

��7������hosts

vi /etc/hosts
���ñ�����hostname��ip��ַ��ӳ��

��8������SecureCRT

��ʱ�Ϳ���ʹ��SecureCRT�ӱ������ӵ���������в�����

һ����˵�����������������virtual box���������������͹��������������һ�㲻��ֱ����virtualbox����ȥ��������Ϊ�Ƚ��鷳��û�а취����ճ��

�����������Ҫ��װ�ܶ�������һЩ������perl��java��redis��storm������һЩ����ֱ��ȥִ��

SecureCRT����windows�������У�ȥ����virtual box�е������

�շѵģ��������������ƽ�棬���ſγ�һ�����ң��ƽ�

��9���رշ���ǽ

service iptables stop
service ip6tables stop
chkconfig iptables off
chkconfig ip6tables off

vi /etc/selinux/config
SELINUX=disabled

�ر�windows�ķ���ǽ

����Ҫ���Ⱥ���еĴ����ݼ����ļ�Ⱥ֮�䣬�ڱ�������˷���ǽ�Ļ������ܻ�û�а취�������ӣ��ᵼ�´ʧ��

��10������yum

yum clean all
yum makecache
yum install wget

------------------------------------------------------------------------------------------

2����ÿ��CentOS�ж���װJava��Perl

WinSCP��������windows��������linux�����֮�以�ഫ���ļ���һ������

��1����װJDK

1����jdk-7u60-linux-i586.rpmͨ��WinSCP�ϴ����������
2����װJDK��rpm -ivh jdk-7u65-linux-i586.rpm
3������jdk��صĻ�������
vi .bashrc
export JAVA_HOME=/usr/java/latest
export PATH=$PATH:$JAVA_HOME/bin
source .bashrc
4������jdk��װ�Ƿ�ɹ���java -version

��2����װPerl

�ིܶʦ�������Լ�֮ǰ���˺ܶ�ʱ����Ժõ������������ȥ���Σ�����ܲ�������

yum install -y gcc

wget http://www.cpan.org/src/5.0/perl-5.16.1.tar.gz
tar -xzf perl-5.16.1.tar.gz
cd perl-5.16.1
./Configure -des -Dprefix=/usr/local/perl
make && make test && make install
perl -v

ΪʲôҪװperl�������������͵�����վ������ҳϵͳ�����ӡ�java+nginx+lua����Ҫperl��

perl����һ�������ı�����Եİ�װ��tomcat����java webӦ��

------------------------------------------------------------------------------------------

3����4��������а�װCentOS��Ⱥ

��1�������������裬�ٰ�װ��̨һģһ��������linux����
��2��������̨������hostname�ֱ�����Ϊeshop-cache02��eshop-cache03��eshop-cache04
��3����װ��֮����ÿ̨������hosts�ļ����棬���ú����еĻ�����ip��ַ��hostname��ӳ���ϵ

����˵����eshop-cache01��hosts����

192.168.31.187 eshop-cache01
192.168.31.xxx eshop-cache02
192.168.31.xxx eshop-cache03
192.168.31.xxx eshop-cache04

------------------------------------------------------------------------------------------

4������4̨CentOSΪssh�����뻥��ͨ��

��1����������̨���������öԱ�����ssh�������¼
ssh-keygen -t rsa
���ɱ����Ĺ�Կ�������в����ûس����ɣ�ssh-keygen����Ĭ�ϻὫ��Կ����/root/.sshĿ¼��
cd /root/.ssh
cp id_rsa.pub authorized_keys
����Կ����Ϊauthorized_keys�ļ�����ʱʹ��ssh���ӱ����Ͳ���Ҫ����������

��2������������̨��������֮���ssh�������¼
ʹ��ssh-copy-id -i hostname��������Ĺ�Կ������ָ��������authorized_keys�ļ���

java���ڹ�˾������Ŀ���м��������Լ�ȥά��linux��Ⱥ�İ�����������

����û�У����ٺ��٣�������һ��Ҫ�������飬��ʵ����SRE����ά��ͬѧ��ȥ����

���Ƕ��ڿγ���˵������ֻ���Լ�һ��һ���������л���ȥѧϰ��������

------------------------------------------------------------------------------------------

�����������linux��Ⱥ��������׼�����ˣ�������4̨�����������������redis��kafka��storm��tomcat��nginx�����л�����