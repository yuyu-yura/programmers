<p>문제 설명
정수 num1과 num2가 매개변수로 주어질 때, num1을 num2로 나눈 값에 1,000을 곱한 후 정수 부분을 return 하도록 soltuion 함수를 완성해주세요.</p>
<p>제한사항
0 &lt; num1 ≤ 100
0 &lt; num2 ≤ 100</p>
<pre><code>def solution(num1, num2):
    sol = (num1 / num2) *1000
    return sol</code></pre><p>틀림 -&gt; int()를 사용하여 소수점 이하를 버리고 정수 부분만 반환을 안함</p>
<pre><code>def solution(num1, num2):
    sol = (num1 / num2) *1000
    return int(sol)</code></pre>