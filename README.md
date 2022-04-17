# login_weniv
## CSS 구현 화면

![image](https://user-images.githubusercontent.com/100753588/163707174-2d99745e-5bfa-4522-8ee7-9b7cdae5de93.png)

## 어려웠던 점, 기억해야할 점
이번에는 어려웠던 점들을 그동안 공부했던 부분들을 통해 스스로 해결하면서 굉장히 뿌듯했다.
검색을 아예 안한건 당연히 아니지만, 배웠던 것중 요 기법을 활용하면 되지 않을까? > 됨 or 안될경우 검색 혹은 스스로 해결할 수 있었기 때문에, css 실력이 성장했음을 느꼈다.

### 1. position relative, absolute 최소한 활용
![image](https://user-images.githubusercontent.com/100753588/163707284-fa58e4fb-bf34-4267-b652-4ac66c6df2c4.png)

최상단 우측의 X 버튼을 제외하고는 확장성에서 취약한 position relative, absolute를 하나도 사용하지 않았다! 뿌듯..
요것도 사용하지 않았더라면 좋았을텐데, float:right; 를 통해 적용했을때 backgroundimage repeat none을 주어도 여백만큼 반복돼서 나타나는 문제가 계속 발생했다..ㅠㅠ


### 2. 가상 클래스 마니마니 연습 !!
![image](https://user-images.githubusercontent.com/100753588/163707219-9a12867c-dec5-4a1f-9aa5-8d057286a320.png)

![image](https://user-images.githubusercontent.com/100753588/163707211-5010cfc8-899a-42de-9de4-86e8de0f9277.png)

굳이 img 태그로 넣지 않아도되는 위와 같은 부분들을 가상 클래스로 삽입하였다.
양옆의 텍스트들과 vertical-align을 사용하여 세로 정렬을 잘 맞춰주었다.

### 3. 마진 병합 현상 발견!!
![image](https://user-images.githubusercontent.com/100753588/163707114-491bd2e0-8f46-435d-9b4a-4e45b7497199.png)

소셜 로그인 버튼 a태그들에 모조리 margin-top을 주어서, 첫번째 버튼인 구글 계정 로그인에는 또는 밑에 줬던 margin-bottom을 빼주어야겠다고 생각했다.
그런데 두둥 놀랍게도 마진 병합현상 덕분에 빼주지 않아도 되는 현상 발견~!

### 4. 이미지 스프라이트 기법 활용 및 세로 정렬
네가지 소셜 로그인 이미지들을 이미지 스프라이트 기법을 처음 활용하여 삽입하였다. 이거 자체는 쉬웠는데....

가장 힘들었던건 텍스트와의 세로 정렬 맞추기였다.
가상 클래스로 이미지들을 넣었는데 자꾸 이상하게 텍스트 위에 빈공간이 생기는것이었다.... display: flex를 활용해서 해결하려니 버튼 텍스트들의 시작점이 모두 동일해지는 문제 발생...
결국 float: left 를 주고, transform: translatey 를 활용하여 이미지를 움직여주는 것으로 해결하였다.

