# red hat ansible 

####Ansible 특징

- **simple** ; IT 인프라의 모든 리소스를 yaml 파일에 풀어서 구현하여 사람이 읽기 용이함 (playbook)

- **powerful** ; Ansible은 python(version 2.x) 으로 구현.

  ​                    python 3.x(내년 하반기 출시예정) 사용가능하나 stable 버전이 아니므로 2.x 권장. 

  example )  python은 인프라와 호환정이 좋기 때문에 python 모듈을 이용하여 기능 구현이 쉬움.

- **agentless** ; ssh 프로토콜을 사용(가상머신에 접속하여 작업)하기 때문에 기술적으로 따지면 agent 를 사용하는 것과 동일 하지만 실제 agent 설치하지 않음.

  직접적인 agent 설치가 없기 때문에 플랫폼으로 부터 자유로워질 수 있음.

 

- **Play book**

  자동화를 위한 정의서 (yaml/json 으로 명시 할 수 있으며 주로 yaml을 사용함)

- **Modules**; tools in toolkit

  python, powershell, any language 에서 제공하는 인프라와 호환 가능한 모듈

- **Inventory** (destination)

  web, db 등 리소스 정보 (default. dns 구성 권장)

- **CMDB**

  다양한 클라우드 리소스 사용 (python 모듈로 구현 되어 있음)



#### play book 

(스페이스바가 중요. 동일한 레벨에서는 동일한 들여쓰기 칸을 맞춘다.)

-------------------

name : install and start apache (어떤 기능을 하는지 )

hosts: all (Inventory의 그룹별 사용 가능)

vars : (변수 정의)

   http_port: 80

remote_user : root  (ssh 접속 계정 정보)



task : 어떤 작업을 할 것 인가

  name : install httpd

  [모듈]

  yum  : pkg=httpd state=latest

...

  template :

  sevices 



#### Ansible Usecase

- Config 설정
- Application deployment (auto build) 기존 Jenkins 혹은 배포툴에 비해 다양한 설정과 동적인 배포 설정 가능
- 프로비저닝; vagrant 를 사용하여 VM 생성 후 Config 설정까지 가능
- Security; Community version 보다 보안에 대한 기능 강화



####Ansible Tower

__________

- Ansible 기반 환경 제어, 사전 정의 된 Play book 제공, GUI를 통한 Ansible 제어를 가능하게 해준다.
- 시각적 Dashboard 제공, 로그 히스토리, 스케쥴러 제공.
- Database 제공. Restful API 제공
- 3rd-party Restful API 연동 가능



**실습**

rht-vmctl status all

vi /etc/hosts

student@workstation 환경

lab tower-install setup (tower vm 실행)

ssh root@tower 접근

inventory 파일에서  그룹명 뒤에 :children 태그를 주면 그룹을 가지는 인벤토리라는 것을 알려줌

adhoc 구성 playbook 내의 단일 명령어 (단일 라인 명령어)

yaml 파일은 전체 설치에 필요한 모든 것을 나열한다.

스페이스바가 중요. 동일한 레벨에서는 동일한 들여쓰기 칸을 맞춰준다.

