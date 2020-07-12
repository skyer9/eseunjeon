# eseunjeon

fork from [https://bitbucket.org/eunjeon/seunjeon/src/master/](https://bitbucket.org/eunjeon/seunjeon/src/master/)

`eunjeon` 에 대한 업데이트는 진행하지 않으며, 단지 `elasticsearch plugin` 유지보수만을 목표로 합니다.

## eunjeon 패키징 방법

```bash
# 사전 다운로드
./scripts/download-dict.sh mecab-ko-dic-2.0.1-20150920

# 버전확인
sbt -version
sbt version in this project: 1.3.5
sbt script version: 1.3.13

# 사전 빌드(mecab-ko-dic/* -> src/main/resources/*.dat)
sbt -J-Xmx2G "runMain org.bitbucket.eunjeon.seunjeon.DictBuilder"

# 테스트
sbt test

# jar 생성
sbt package
```

## eseunjeon 패키징 방법

```bash
./gradlew build
```
