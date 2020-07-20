* symbolic link의 소유자 및 group 소유자를 바꾸고 싶을 때 
$ chown -h user_name:group_name path/to/file 

-h 옵션이 빠지면, symbolic link의 원본 타겟에 대한 소유자 변경

* symbolic link에 대한 chmod 
chmod로 symbolic link에 대한 소유 권한을 변경하는 것은 의미가 없음