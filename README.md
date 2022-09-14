.gitignore

# 모든 file.c

file.c

# 최상위 폴더의 file.c

/file.c

# 모든 .c 확장자 파일

\*.c

# .c 확장자지만 무시하지 않을 파일

!not_ignore_this.c

# logs란 이름의 파일 또는 폴더와 그 내용들

logs

# logs란 이름의 폴더와 그 내용들

logs/

# logs 폴더 바로 안의 debug.log와 .c 파일들

logs/debug.log
logs/\*.c

# logs 폴더 바로 안, 또는 그 안의 다른 폴더(들) 안의 debug.log

logs/\*\*/debug.log
