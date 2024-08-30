# IssueList
Issue List in Android Studio [ 2024.08.30~ ]

1. ScrollView with RecyclerView (스크롤 뷰와 리사이클러 뷰를 같이 쓸 경우)
 - When using RecyclerView inside ScrollView, scrolling and viewing problems occur.
 - For example, if there are 4 items in RecyclerView, only 2 can be visible.
 - The solution is to change "ScrollView" to "NestedScrollView".

 - ScrollView 안에 RecyclerView를 사용할 경우, 스크롤 문제나 뷰에 관한 문제가 발생합니다.
 - 예를 들어, RecyclerView안에 4개 아이템이 있는데, 2개만 보이는 경우가 있습니다.
 - 이 경우, ScrollView를 NestedScrollView로 변경하면 해결됩니다.
   
2. Assigning a listeners inside a loop may cause malfunction (반복문 안에서 리스너를 할당할 경우, 오작동 발생)
 - When developing, there are cases where there are multiple buttons that perform the same function.
 - Usually, the listener is assigned through the parent view and a loop.
 - In this case, it may or may not malfunction due to differences in the compilers of MacOS and WindowOS.
 - The problem can be solved by passing parameters as [final] through a separate function.

 - 개발을 하다보면, 같은 기능을 수행하는 버튼이 여러 개인 경우가 있습니다.
 - 보통 이럴 때에는 Parent View를 가져와, 반복문과 getChildCount(), getChildAt() 등을 이용해 리스너를 할당하기도 합니다.
 - 이 경우, MacOS에서는 정상동작 하지만, WindowsOS에서는 리스너 내부에서 사용하는 반복문의 index가 오작동을 일으킬 수 있습니다.
 - 해결 방법은, 별도 함수에서 파라미터로 상수를 전달 받아 할당하면 해결된다.

3. 
