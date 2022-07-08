# hello git

## git 명령어 요약

- clone: 원격 저장소 (github) 을 내 컴퓨터에 복사해 온다.
- add: 내 컴퓨터에서 작업한 파일들을 스테이지에 추가
- commit: 스테이지에 올라온 파일들을 가지고 내 컴퓨터에 저장 (세이브와 같다.)
- push: 커밋들을 원격 저장소에 업로드

## 파일의 내용 되돌리기

- 특정 파일의 내용을 마지막 커밋으로 돌리고 싶다면 해당 파일 선택 후 '코드 뭉치 버리기' 선택

## 브랜치 변경하기

- 브랜치 : 기존 내용을 유지한 채 새로운 내용을 추가하고 싶을 때 사용.
- 체크아웃 : 특정 브랜치(혹은 커밋)으로 돌아가고 싶을 때 사용.
- 소스트리의 체크아웃 : 프랜치 이름을 더블 클릭하는 것만으로 체크아웃 가능


## 병합하기 1

- 헤드 브랜치에 변경사항이 없고
- 병합 대상 브랜치가 헤드로부터 시작된 경우
- 아주 쉽게 병합가능 = Fast-forward

## 병합하기 2

- 헤드 브랜치에 추가적인 커밋이 생기는 경우
- 진짜 병합이 필요해 진다.
- 충돌이 안 나면 좋지만, 충돌이 나도 겁내지 말자.

## 커밋 되돌리기

### reset 사용하기

- 장점 : 쉬어요.
- 단점1: 커밋이 날아감.
- 단점2: 강제 푸시가 필요함.

### branch 만들어서 되돌리기

- reset과는 달리 내용이 사라지지 않는다.
- 장점 : 쉽다.
- 단점 : 트리가 지저분해진다.

### revert

- 역시 커밋은 없어지지 않는다.
- 장점: 가장 정석적
- 단점: 충돌이 날 수 있다.


### revert 2 

- revert로 여러 커밋을 되돌리려면 최신부터 순서대로 revert 하자
- 그렇게 하면 충돌을 막을 수 있다.

## 커밋 덮어쓰기

- 필요하다면 이전 커밋 덮어쓰기도 가능
- 'commit --amend'
- 이미 push를 한 경우 'push --force'가 필요함

## stash 

- 다른 브랜치로 체크아웃하기 전에 현재 작업내용을 저장하는 임시 저장소
- 유용하니 잘 사용하자.