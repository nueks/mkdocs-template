
## 사용법

1. 현재 repo 를 clone 해서 .git 디렉토리를 삭제하고
   `git init` 부터 실행해준다.
1. `mkdocs.yaml` 파일이 설정파일이다. 이 파일을 적당히 수정해준다.
1. `Settings` --> `Pages` 에서 `gh-pages` 를 source 로 설정한다.
1. `Actions` 로 동작하는 설정이기 때문에 파일을 push 하면 자동으로 `mkdocs build` 를 수행해서
   `gh-pages` 브랜치로 문서를 배포해준다.


## Live Preview
`mkdocs.yaml` 파일이 있는 위치에서 다음 명령을 수행한다.

**using docker**
```sh
docker run --rm -it -p 8000:8000 -v $(pwd):/docs squidfunk/mkdocs-material
```

docker 를 사용하지 않으려면 pip로 패키지를 설치하고, 직접 실행하면 된다.
```sh
pip install mkdocs-material=="8.*"
```

```sh
mkdocs serve
```


## Sample

- [test](test)
