# :fire: 개요
주환군의 블로그 프로젝트
# :computer: 개발 정보
- 맡은 분야: 퍼블리싱
- Editor: Visual Studio Code
- 사용언어: HTML5, CSS3, JavaScript, SCSS
# :page_facing_up: 규칙
## CSS
- html의 기본 font-size는 10px이며, 자식 요소들의 font-size 단위는 rem으로 통일합니다.
> font-size 16px -> 1.6rem, 14px -> 1.4rem
## SCSS
1. css파일은 `/resource/css` 에 위치합니다.
2. scss파일은 `/resource/css/scss` 에 위치합니다.
3. css로 컴파일시 compressed 버전(.min.css)으로 설정합니다.
### setting.json
만약 VS Code의 `Live SASS 6.0.0` 을 사용하시면 setting.json 을 아래와 같이 수정합니다.
```json
{
    "liveSassCompile.settings.formats":[
        {
            "format": "expanded",
            "extensionName": ".css",
            "savePath": "~/../"
        },
        {
            "format": "compressed",
            "extensionName": ".min.css",
            "savePath": "~/../"
        },
    ],
    "liveSassCompile.settings.excludeList": [ 
        "**/node_modules/**",
        ".vscode/**" 
    ],
    "liveSassCompile.settings.autoprefix": [
        "> 1%",
        "last 2 versions"
    ],
    "liveSassCompile.settings.generateMap": false
}
```
