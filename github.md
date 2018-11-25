github 사용시 발생한 에러들

1. 기본
  git init
  git add *
  git commit -m "init"
  git push origin master
  git remote add orignin < 원격 서버 주소 >

  git checkout -b feature_x (생성)
  git checkout master (master로 이동)
  git branch -d feature_x (삭제)
  git push origin < 가지 이름 >


2. .gitignore

# 기본 명령어
  *.a       # no .a files
  !lib.a    # but do track lib.a, even though you're ignoring .a files above
  /TODO     # only ignore the root TODO file, not subdir/TODO
  build/    # ignore all files in the build/ directory
  doc/*.txt # ignore doc/notes.txt, but not doc/server/arch.txt


출처: http://emflant.tistory.com/127 [SourceBox]
# 변경사항이 반영 안될때
  git rm -r --cached .
  git add .
  git commit -m "your commit message”

# 이미 커밋된 파일 무시
$ git rm --cached log.txt
$ git commit -m 'untrack log.txt'

