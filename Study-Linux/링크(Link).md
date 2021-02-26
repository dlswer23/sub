## 링크(Link)

+ 파일의 링크(Link)에는 하드 링크(Hard Link) 와 심볼릭 링크(Symbolic Link 또는 Soft Link) 두 가지가 있음

![Link](https://blog.kakaocdn.net/dn/btDb1B/btqDFpHttQU/cMTWYDernvubyOVWs983PK/img.png)
+ 하드 링크를 생성라면 "하드링크파일" 만 하나 생성되며 같은 inode1을 사용
  + (명령 : #In 링크대상파일이름 링크파일이름)
+ 심볼릭 링크를 생성하면 새로운 inode2를 만들고, 데이터는 원본 파일을 연결하는 효과 
  + (명령 : #In -s 링크대상파일이름 링크파일이름 )

