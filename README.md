# 기술블로그 시작

> jekyll 활용해 블로그 만들면서 오류해결

유레카 프로젝트 수업시간에 다뤘던 Jekyll 설치 부분은 제외하였습니다.  
<br>
<br>
테마적용 부터
![alt text](/public/img/screenshot-1.png)

계속해서 원인모를 에러가나서 겨우 찾은 Monos 테마  
[퍼온 깃허브 주소](https://github.com/ejjoo/jekyll-theme-monos)

---

## Error 1 : Could not find addressable -2.7.0

<br>

![alt text](/public/img/2022-11-30-start/adressable.png)

addressable 버전이 달라서 생기는 문제라고 한다.
<br/>
<br/>

```
sudo gem install "addressable:~> 2.7.0"
```

버전에 맞게 설치해주니 해결이 되었다.  
<br>

---

## Error 2 : Could not find concurrent-ruby

<br/>
<br/>

![alt text](/public/img/2022-11-30-start/find_ruby.png)

이번엔 루비를 찾을수 없다그런다.  
블로그 여기저기 찾아보니 아마 _bundler_ 에서 오류가 생긴것 같다.  
<br/>

```
bundle update
```

간단하게 해결  
<br>

---

## Error 3 : You have already activated mercenary 0.4.0 but your Gemfile requires mercenary 0.3.6. Prepending 'bundle exec' to your command may solve this.

<br/>
<br/>
친절하게 bundle exec를 실행하라고 코드에 써져있다.
<br>
<br>

```
bundle exec jekyll serve
```

로 코드를 실행시켜주니 자동으로 해결이 되었다.

# 블로그 제목 및 sidebar 변경

제목과 한줄소개 부분은 `config.yml` 에서 쉽게 바꿀 수 있었다.  
sidebar의 categories 부분은 글을 쓸때, `markdown file`의 `header` 부분에 `category` 항목이 있는데 자동으로 반영되어 생긴다.
<br>
<br>
pages부분은 아직 발견을 못하여 관련된 코드 부분을 비활성화 시켰다.

# favicon 설정

검색을 통하여 파비콘을 생성해주는 favicon-generator.org 사이트를 발견하였고, 이미지는 아이디 맨앞글자인 B를 사용하였다.
파비콘 설정 중 캐시가 남아있어 일부 경로에 적용이 안되었으나, 캐시파일을 지우고나니 접속이 원할하게 되었다.

## 완성 사진(블로그 제목은 바꿨음)

![alt text](/public/img/readme/readMe.png)

# 후기

깃 블로그 장점 : 처음부터 원하는대로 만들 수 있다.  
깃 블로그 단점 : 처음부터 전부 만들어야한다.

naver blog는 너무 제약이많고 git blog는 너무 할게 많아서, tistory 한번 써보고 git blog쓸지 tistory쓸지 결정해야겠다.
