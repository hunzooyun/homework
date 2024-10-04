# Git에 대해 배운것들의 간단한 정리

## CLI 명령어 모음

| 명령어                                       | 설명                                        |
| :------------------------------------------- | :------------------------------------------ |
| ls                                           | 파일보기                                    |
| ls -a                                        | 숨겨진 파일 확인                            |
| cd                                           | root directory로 이동                       |
| cd .                                         | 현재 directory                              |
| cd ..                                        | 부모 directory                              |
| pwd                                          | 현재 directory 확인                         |
| clear                                        | terminal 입력 내용 지우기                   |
| touch [file_name]                            | 빈 file 생성                                |
| echo "내용">>[file]                          | 내용을 file 속에 집어넣기                   |
| mkdir [dir_name]                             | directory 생성                              |
| cat [file_name]                              | file 내용 확인                              |
| mv [file_name or dic_name] [target_dir_name] | target directory로 file or directory 옮기기 |
| mv [file_name or dic_name] [new_file_name]   | file or directory 이름 바꾸기               |
| cp [file] [target_dir_name]                  | 복사                                        |
| cp -r [folder_name]                          | 복사                                        |
| rm [file_name]                               | file 삭제                                   |
| rm -r [dir_name]                             | directory 삭제                              |
| **rm -rf**                                   | **경고무시하고** 삭제                       |
| code .                                       | 현재 directory를 VSC에서 열기               |
| &&                                           | 한번에 여러 명령 내리기                     |

### 명령어 만들기

code ~/.bashrc 오픈 후
take() {
mkdir -p "$1" && cd "$1"
}
저장
ctrl+shift+p reload

안될경우
code ~/.bash+profile
take() {
mkdir -p "$1" && cd "$1"
}
저장 후 종료하고 다시 켜기

## Git 명령어 모음

| 명령어                                      | 설명                                                         |
| :------------------------------------------ | :----------------------------------------------------------- |
| git init                                    | 저장소 생성                                                  |
| git config --global user.name               | 이름 확인                                                    |
| git config user.name                        | 확인하는 방법                                                |
| git config --global init.defaultBranch main | 전체적인 기본 설정                                           |
| git config --global core.autocrlf true      | 자동줄바꿈                                                   |
| git config --list                           | 설정확인                                                     |
| git status                                  | 파일 상태 확인                                               |
| git add                                     | sa에 파일 추가                                               |
| git add .                                   | 현재 변경사항 전부 sa에 올리기                               |
| git commit                                  | sa에 올라온 파일 확정하기                                    |
| git commit -m "커밋메시지"                  | 커밋메시지로 바로 확정하기                                   |
| git commit -am "커밋메시지"                 | sa를 거치지 않고 바로 확정하기                               |
| git log                                     | 현재 위치한 branch commit 내용 확인                          |
| git log --oneline                           | 현재 위치한 branch commit 내용 한줄로 확인                   |
| git log --graph                             | 현재 위치한 branch commit 내용 그래프로 확인                 |
| git log --all                               | 현재 위치한 branch commit 내용 전부 확인                     |
| git rm --cached                             | root commit이 없는 상태에서 이전 상태로 복원                 |
| git restore --staged                        | sa에 올라간 file을 wd로 다시 돌려보내기                      |
| git restore                                 | 작업 내용 취소                                               |
| git diff                                    | 파일 변경내용 비교하기                                       |
| git branch                                  | branch 조회                                                  |
| git branch -c                               | branch 생성                                                  |
| git branch -d                               | branch 삭제                                                  |
| git switch                                  | branch로 이동                                                |
| git switch -c                               | branch로 생성&이동                                           |
| git checkout -b                             | branch 생성&이동                                             |
| git reset HEAD~숫자                         | 커밋기록은 삭제하지만 wd에 변경사항 남기기                   |
| git reset --soft HEAD~숫자                  | 커밋기록은 삭제되지만 wd와 sa에 변경사항 남기기              |
| git reset --hard HEAD~숫자                  | 숫자만큼 전으로 이동하고 그 뒤로 변경된 커밋기록은 모두 삭제 |
| git merge                                   | branch 병합                                                  |
| git merge --abort                           | branch 병합 취소                                             |
| git checkout 해시태그                       | 해시태그 위치로 이동                                         |
| git push                                    | local의 변경사항을 remote로 전송                             |
| git push origin main                        | main branch를 remote 서버에 전송                             |
| git pull origin main                        | remote에 저장된 branch의 현재 상태를 다운받고 main으로 병합  |
| git remote add origin <원격주소>            | 클라우드 주소 등록                                           |
| git clone URL                               | URL 소스 코드 다운로드&복제                                  |
| git clone /로컬/저장소/경로                 | 로컬 저장소 복제                                             |
| degit url ./폴더명                          | 해당폴더로 url 파일 다운                                     |
| git config --global -e                      | 환경설정                                                     |
| git config --global pager.log "less -FRX"   | 바로 끝내기                                                  |
