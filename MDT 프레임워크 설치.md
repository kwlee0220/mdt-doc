


# MDT 프레임워크 및 클라이언트 설치
본 문서는 MDT 프레임워크 및 클라이언트 설치 과정을 설명한다. 본 문서는 제공되는 SW가 설치된 최상위 디렉토리가 $HOME/mdt (Windows인 경우에는 C:\mdt) 인 것을 가정하고 기술한다. 그러나 이것은 반드시 해당 위치에 설치될 필요는 없고, 다른 디렉토리에 설치되어도 무방하다.

제공되는 MDT 프레임워크와 클라이언트는 각각 다른 컴퓨터에 설치될 수 있으나 본 문서에서는 설명의 편의상 동일 컴퓨터에 설치되는 것을 가정한다.

제공되는 S/W의 구성은 다음과 같다.

 - mdt-manager: MDT 프레임워크 서버
 - client: MDT 프레임워크 클라이언트
 - operation-server: HTTP 기반 MDT 연산 수행 서버
 - models: S/W와 함께 제공되는 샘플 MDT 인스턴스 모델

## **MDT 프레임워크 서버 (mdt-manager) 설치**
MDT 프레임워크 서버 설치를 통해 운영되는 모듈을 다음과 같다.
- MDTInstance 관리자
-  AssetAdministrationShell registry
-  Submodel registry
- MDT 워크플로우 관리자

### 설치과정
 1. mdt-manager가 설치된 디렉토리 ($Home/mdt/mdt-manager)로 이동한다
 2. Text editor를 사용하여 ‘application.yml’ 파일을 열어 필요한 부분을 설정한다.
	 1.  ‘server’ 항목의 ‘host’ 부분을 MDT 프레임워크 서버가 설치된 호스트 IP 주소를 설정한다.
	 2. (Optional) ‘server’ 항목의 ‘port’부분을 MDT 프레임워크 서버가 구동될 때 사용할 소켓 포트 번호를 설정한다. 특별한 이유가 있지 않는 경우 현재 기본 값인 12985를 사용하는 것을 권장한다.
	 3. ‘rootDir’ 항목에 MDT 프레임워크 SW가 설치된 최상위 디렉토리 경로명을 설정한다.

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMDgzMDE0MTNdfQ==
-->