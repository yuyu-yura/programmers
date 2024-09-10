<p>문제 설명
정수 n이 주어질 때, n이하의 짝수를 모두 더한 값을 return 하도록 solution 함수를 작성해주세요.</p>
<p>제한사항
0 &lt; n ≤ 1000</p>
<pre><code>def solution(n):
    if 0 &lt; n &lt;= 1000:
        sol = 0
        for i in range(1+n):
            if i % 2 == 0:
                sol += i
    return sol</code></pre><p>틀림 :
위 문제에서는 1부터 n까지의 짝수를 검사해야 하므로, range(1, n+1)을 사용해야 합니다. range(n+1)을 사용하면 0도 포함되기 때문에, 짝수를 검사할 때 0이 포함될 수 있습니다.</p>
<pre><code>def solution(n):
    if 0 &lt; n &lt;= 1000:
        sol = 0
        for i in range(1,1+n):
            if i % 2 == 0:
                sol += i
    return sol</code></pre><blockquote>
<p>+= 연산자는 더해서 변수에 다시 저장하는 역할</p>
</blockquote>
<blockquote>
<p>i는 반복문에서 사용하는 루프 변수
이 변수는 반복문이 실행될 때마다 일정한 값을 가지며, 일반적으로 반복문에서 순차적으로 값을 증가시키면서 사용</p>
</blockquote>
<ul>
<li><p>range 함수의 기본 형태:
range(stop):</p>
<p>0부터 stop-1까지의 정수를 생성합니다.
예: range(5)는 [0, 1, 2, 3, 4]를 생성합니다.
range(start, stop):</p>
<p>start부터 stop-1까지의 정수를 생성합니다.
예: range(2, 5)는 [2, 3, 4]를 생성합니다.
range(start, stop, step):</p>
<p>start부터 stop-1까지의 정수를 step 간격으로 생성합니다.
예: range(0, 10, 2)는 [0, 2, 4, 6, 8]를 생성합니다.</p>
</li>
<li><p>range(1, n+1)과 range(n+1)의 차이점
두 표현 모두 range 함수를 사용하지만, 그 동작 방식은 다릅니다.</p>
<p>range(1, n+1):
시작값: 1부터 시작합니다.
끝값: n+1까지 포함하되, n+1은 포함하지 않습니다. 따라서 1부터 n까지의 값을 생성합니다.
예시: 만약 n = 5라면, range(1, 6)은 [1, 2, 3, 4, 5]를 생성합니다.
range(n+1):
시작값: 기본적으로 0부터 시작합니다.
끝값: n+1까지 포함하되, n+1은 포함하지 않습니다. 따라서 0부터 n까지의 값을 생성합니다.
예시: 만약 n = 5라면, range(6)은 [0, 1, 2, 3, 4, 5]를 생성합니다.
차이점:
range(1, n+1)은 1부터 n까지의 값을 생성하며, 0은 포함하지 않습니다.
range(n+1)은 0부터 n까지의 값을 생성합니다.</p>
</li>
</ul>