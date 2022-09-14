# OCI_code

Oracle Cloud Free Tier 가입

https://www.oracle.com/kr/cloud/

  https://docs.oracle.com/en-us/iaas/Content/Compute/References/computeshapes.htm
  
  OCI 기본용어 http://taewan.kim/oci_docs/00_oci/terminologies/

  OCPU (Oracle ComPute Unit)

리소스실행 > VM 인스턴스 생성 > VM.Standard.E2.1.Micro (Free)

  가상 머신, 1 core OCPU, 1 GB memory, 0.48 Gbps network bandwidth

이미지 및 구성 > 편집 > 이미지 변경

공용 IPv4 주소

공용 IP 주소를 지정하면 인터넷에서 이 인스턴스에 액세스할 수 있게 됩니다. 공용 IP 주소가 필요한지 여부를 모를 경우 항상 나중에 지정할 수 있습니다.

인스턴스 생성 완료 후

리소스 _ VINC _ 인스턴스네임 _ 리소스 _ IPv4 _ 편집에서 공용(인스턴스 종료_삭제시 만료되어 사용불가) IPv4 주소를 예약된 주소로 변경가능

https://docs.oracle.com/en-us/iaas/Content/Network/Tasks/managingpublicIPs.htm

SSH 키 추가 > 자동으로 키 쌍 생성 > 전용, 공용 키 저장

-------------------------

SSH 키 쌍을 자동으로 생성하여 저장한 경우

PuTTYgen > Load > all files > *.key 선택 > Successfully imported > Save private key

Putty > SSH > Auth > Browse... > 

--------------------------

pwd > /homw/ubuntu

code server 설치

$sudo curl -fsSL https://code-server.dev/install.sh | sh

  + mkdir -p ~/.cache/code-server
  
  + curl -#fL -o ~/.cache/code-server/code-server_4.7.0_amd64.deb.incomplete -C -https://github.com/coder/code-server/releases/download/v4.7.0/code-server_4.7.0_amd64.deb

  + mv ~/.cache/code-server/code-server_4.7.0_amd64.deb.incomplete ~/.cache/code-server/code-server_4.7.0_amd64.deb
  
  + sudo dpkg -i ~/.cache/code-server/code-server_4.7.0_amd64.deb

$code-server

   info Wrote default config file to ~/.config/code-server/config.yaml

Ubuntu 실행시 code-server가 자동 실행 되도록 service 등록!


