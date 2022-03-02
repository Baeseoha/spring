## jqGrid로 Header grouping 하는 방법

참고 사이트 - https://1004lucifer.blogspot.com/2019/05/jqgrid-header-grouping.html?showComment=1646184844514#c4258347210958832269

참고 사이트를 보고 제가 사용하는 jqGrid에 적용시켜봤어요.

결과 표입니다. 이렇게 만들고자 시도했습니다.
![bill](https://user-images.githubusercontent.com/65885458/156362892-8cfef873-da2b-4375-b2d9-0a463f02b872.png)

표의 id 값이 #gridList로 되어있고, 시작 name을 지정해준뒤 그룹핑할 컬럼 갯수를 바꿔주면 끝 
 
'''
$("#gridList").jqGrid('setGroupHeaders', {
        useColSpanStyle: true, 
        groupHeaders:[
          {startColumnName: 'prcPlyScl', numberOfColumns: 3, titleText: '<center>요금정책</center>'}
        ]  
   });

'''

이렇게 컬럼 그룹핑은 성공했으나, 밑의 내용과 너비가 안맞는 문제 발생

https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=aladdin76&logNo=40188171190

해당 블로그를 보고 해결했습니다.

저는 shrinkToFit을 false로만 바꿔줬더니 너비가 잘 맞았어요.







