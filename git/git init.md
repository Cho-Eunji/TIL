## `git init`으로 second-repo만드는 방법

## Commands

```shell
$ mkdir second-repo
$ git init
//여기서 git remote하면 아무것도 안나옴 (why? 받는 이를 안 썼기 때문!)
// github에서 remote repo를 생성한 뒤,
$ git remote add mask {repo_url}
// <git remote add {별명} {주소}> 관습적으로 origin 많이 씀 / remote로 보내겠다고 연결만 해둔 상태

// After doing some work,
$ touch README.md
//vi로 README.md 수정
$ git add {filename}
$ git commit

$ git branch -M main
//branch이름이 master로 되어있기 때문에 github에 맞춰주려면 main으로 바꿔줘야함
$ git push -u mask main
//clone은 remote에 있는걸 그대로 복제 해와서 건드릴 필요 없지만 
//init방식은 각각 존재한 거고 이름만 같고 실질적인 상관 관계를 만들어준 적 없기 때문에 -u(upstream set)를 통해 연결해주는 것
```
