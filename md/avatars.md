# 2주차 과제

## Avatars 과제 링크

[Avatars.html](./../avatars/avatars.html)  
[Avatars.css](./../avatars/styles/avatars.css)

## Avatars 과제에 대하여

과제를 받았을때 선생님이 처음에 어떻게 영역을 나눠야 될지 생각해보라고 하셔서 box를 하나 만들어서 테두리를 만들고 margin을 통해 가운데로 몰아야겠다고 생각했습니다.  
과제 조건을 잊지 않기 위해서 조건을 따로 dl로 정리해두었습니다.  
첫 번째 과제인 float를 만들어보기 시작했습니다.  
2번째 조건인 성능 최적화를 해보기 위해서 인터넷을 통하여 avif파일과 webp 파일로 변환을 시켜서 다운 받았고 picture를 통하여 3가지를 한번에 묶어서 img들을 일렬로 정렬했습니다.  
상태정보인 초록불과 회색불을 어떻게 넣으면 될까 하다가 span에 class를 줘서 따로 색깔을 넣으면 되겠다는 생각으로 offline과 online을 만들었고 picture와 한 셋트이기 때문에 span으로 묶었습니다.  
추가로 상태정보를 avatar 우측하단에 보이게 하기 위해서 부모요소인 span에 position=relative를 주고 class가 부여된 span에 position=absolute를 주어서 top과 left를 통해 위치를 이동시켰습니다.  
2번째 과제인 flex는 사용방법을 몰라서 인터넷에서 찾아보고 display: flex;를 설정하고 jstify-content: space-between을 통하여 box에 avatar를 간격두고 배치하였습니다.  
2개를 한곳에 하려니 flex 상태정보가 위에 올라가 있어서 css에 .flex를 추가하여 한번 더 위치조정을 해주었습니다.
