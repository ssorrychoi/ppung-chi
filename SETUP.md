# 뿡치 웹사이트

모바일 서프라이즈 초대장. 별도 빌드 없이 index.html과 ppungppung.png로 실행됩니다.

## GitHub Pages

Settings → Pages → Deploy from a branch → main → /(root) → Save.

## Firebase

프로젝트: ppung-chi

- Authentication에서 Anonymous 로그인을 활성화합니다.
- Firestore 기본 데이터베이스를 생성합니다.
- firestore.rules의 내용을 Firestore 규칙에 적용합니다.
- 방문자의 이름, 메시지, 익명 사용자 UID, 서버 작성 시각을 messages/{uid}에 저장합니다.
- 익명 계정당 편지 하나를 생성합니다. 방문자는 다른 사람의 편지를 조회할 수 없습니다.
- 저장된 편지는 소유자가 Firebase 콘솔에서 확인합니다.
- Firebase 웹 구성은 공개 클라이언트 설정입니다. 보안은 Firestore 규칙으로 적용합니다.

## 확인

사이트에서 마지막 화면까지 이동하여 편지를 저장한 뒤 Firestore 콘솔의 messages 컬렉션에서 확인합니다.

## 파일

- index.html: 스타일과 전체 인터랙션, Firebase 연결
- ppungppung.png: 사용자가 제공한 이미지
- firestore.rules: 데이터 접근 규칙
