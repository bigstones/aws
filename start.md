### aws console 에서 EC2를 생성한다.

    팁
    - 스팟인스턴스를 사용하면 과금이 적다
    - 스팟인스턴스는 종료설정, 종료방지 설정을 할 수 없다
    
### MacBook에서는 terminal을 이용해 바로 ssh 접속이 가능하다

    ssh -i [pem 파일경로] [유저명]@[Public IP 또는 Public Domain]
    
### 유저명은 EC2 아마존 이미지마다 상이하다.

    Amazon Linux | ec2-user
    CentOS | centos
    Debian | admin
    Fedora | ec2-user or fedora
    RHEL | ec2-user or root
    SUSE | ec2-user or root
    Ubuntu | ubuntu
   
### .ssh/config 파일 설정을 통해 간단하게 접속할 수도 있다.

ssh config 파일 수정

    $ vi ~/.ssh/config
    
다음과 같이 편집

    Host [서비스명]
        HostName [Public IP or Public Domain]
        User [유저명]
        IdentityFile [pem 파일경로]

vi를 빠져나와 다음명령어를 실행하면 된다.

    $ chomod 700 ~/.ssh/config
    $ ssh [서비스명]
    
    
초기에는 sudo [apt/dpkg/yum/rpm]을 업데이트해준다.
