# Web_study
 
## 실습 : 도서대여예약 (bookRental.html) 
 
 - html5, 모든 입력 항목은 필수항목 
 - pattern 반영 
 
 - 아이디 : 영문대소문자숫자조합, 최소 6자리, 최대 30자리
 - 휴대폰 : 010-0000-0000
 - 이메일 : 000@0000.000
 - 도서명 : 
 - 예약권수 : 최소 1권 최대 5권 
 - 예약 희망날짜 : 현재날자 기본 
 - 도서 수령시간 : (09시~17시 사이)
 
## html5 구조
<pre> 
<code>

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>도서대여예약</title>
</head>
<body>
<h3>HTML5 실습</h3>
<h3>도서대여예약</h3>
<table border="1" cellspacing="5px" cellpadding="5px">
<form action ="joinResult.html" method="post">

	<!-- 아이디 : 영문대소문자숫자조합, 최소 6자리, 최대 30자리 -->
	<tr>
	<td>아이디</td>
	<td><input type="text" name="memberId" autofocus="autofocus" required="required"
			   pattern="[A-Za-z0-9]{6,30}" placeholder="영문대소문자, 숫자조합, 6~30자리">
			   </td>
	</tr>
	
	<!-- 휴대폰 : 010-0000-0000 -->	
	<tr>
		<td>휴대폰</td>
		<td><input type="moblie" name="mobile" required="required" 
				   pattern="010-\d{4}-\d{4}" placeholder="010-0000-0000">
				   </td>
	</tr>
	
	<!-- 이메일 : 000@0000.000 -->
	<tr>
		<td>이메일</td>
		<td><input type="email" name="email" required="required"
				   placeholder="aaa@aaa.com">
		</td>
	</tr>
	
	<!-- 도서명 -->
	<tr>
		<td>도서명</td>
		<td><input type="text" name="bookName" required="required"
				   placeholder="도서명 입력">
		</td>
	</tr>
			
	<!-- 예약권수 : 최소 1권 최대 5권  -->	
	<tr>
		<td>예약권수</td>
		<td><input type="number" name="bookCount" required="required"
				   min="1" max="5" value="1">
		</td>
	</tr>
		
	<!-- 예약 희망날짜 : 현재날자 기본   -->
	<!-- 시스템 날짜 구현 방법은 모르겠다 찾아보는 중 -->
	<tr>
		<td>예약 희망날짜</td>
		<td><input type="date" name="bookingDate" required="required" 
				   value="2021-06-26">
		</td>
	</tr>	
	<!-- 도서 수령시간 : (09시~17시 사이)  -->		
	<tr>
		<td>도서 수령시간</td>
		<td><input type="time" name="time" required="required"
				   min="09:00" max="17:00" value="09:00"
				   style="width:120px;">
		</td>
	</tr>			
			
				   	
	<!--  submit/reset -->
	<tr>
		<td colspan="3" align="right">
			<input type="submit" value="예약">
			<input type="reset" value="취소">
		</td>

</form>

</table>


</body>
</html>

</code>
</pre>

## html5 스크립트


<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>도서대여예약</title>
</head>
<body>
<h3>HTML5 실습</h3>
<h3>도서대여예약</h3>
<table border="1" cellspacing="5px" cellpadding="5px">
<form action ="joinResult.html" method="post">

	<!-- 아이디 : 영문대소문자숫자조합, 최소 6자리, 최대 30자리 -->
	<tr>
	<td>아이디</td>
	<td><input type="text" name="memberId" autofocus="autofocus" required="required"
			   pattern="[A-Za-z0-9]{6,30}" placeholder="영문대소문자, 숫자조합, 6~30자리">
			   </td>
	</tr>
	
	<!-- 휴대폰 : 010-0000-0000 -->	
	<tr>
		<td>휴대폰</td>
		<td><input type="moblie" name="mobile" required="required" 
				   pattern="010-\d{4}-\d{4}" placeholder="010-0000-0000">
				   </td>
	</tr>
	
	<!-- 이메일 : 000@0000.000 -->
	<tr>
		<td>이메일</td>
		<td><input type="email" name="email" required="required"
				   placeholder="aaa@aaa.com">
		</td>
	</tr>
	
	<!-- 도서명 -->
	<tr>
		<td>도서명</td>
		<td><input type="text" name="bookName" required="required"
				   placeholder="도서명 입력">
		</td>
	</tr>
			
	<!-- 예약권수 : 최소 1권 최대 5권  -->	
	<tr>
		<td>예약권수</td>
		<td><input type="number" name="bookCount" required="required"
				   min="1" max="5" value="1">
		</td>
	</tr>
		
	<!-- 예약 희망날짜 : 현재날자 기본   -->
	<!-- 시스템 날짜 구현 방법은 모르겠다 찾아보는 중 -->
	<tr>
		<td>예약 희망날짜</td>
		<td><input type="date" name="bookingDate" required="required" 
				   value="2021-06-26">
		</td>
	</tr>	
	<!-- 도서 수령시간 : (09시~17시 사이)  -->		
	<tr>
		<td>도서 수령시간</td>
		<td><input type="time" name="time" required="required"
				   min="09:00" max="17:00" value="09:00"
				   style="width:120px;">
		</td>
	</tr>			
			
				   	
	<!--  submit/reset -->
	<tr>
		<td colspan="3" align="right">
			<input type="submit" value="예약">
			<input type="reset" value="취소">
		</td>

</form>

</table>


</body>
</html>


