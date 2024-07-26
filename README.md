# coTe
프로그래머스

### 99클럽 코테 스터디 1일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 까먹은 자바 기본 문법 다시 리콜
    * 세미콜론 자꾸 까먹음
- 공부한 내용 본인의 언어로 정리하기
    * 코틀린으로 하면 솔직히 좀 간단한 것 같음ㅋㅋㅋ.....

```
    class Solution {
        fun solution(n: Long): IntArray {
            return n.toString()
                .map { it.toString().toInt() }
                .reversed()
                .toIntArray()
        }
    }
```

- 오늘의 회고
  * 예전 기억이 떠올라서 나누기 10해서 하는 방식 하려다가
  그냥 간단히 스트링화시켜서 자르는걸 선택했다.

  * 업무
    - InputStream, Buffer 사용할때 습관적으로 close를 해야하는데, 코틀린에서는 use 블록으로 해당 객체가 종료될 때 자동으로 close()를 호출하는 함수를 사용할 수 있다.
    close()를 생략해도 객체가 사용된 메서드가 종료될 때 GC가 정리한다고는 하는데, 그래도 명시적으로 close()를 호출하는 것이 좋다.




### 99클럽 코테 스터디 2일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 또 세미콜론
    * 오늘은 할 말이 없음 lvl 0...
- 공부한 내용 본인의 언어로 정리하기
    * 하하...코틀린은 함수가 있어서..간단합니다

```
class Solution {
    fun solution(arr: Array<Int>): Double {
        return arr.average()
    }
}
```

- 오늘의 회고
    * 왜 이틀째가 더 쉬워졌지

    * 업무
    - 로그 세팅 파일좀 열어봐야지

### 99클럽 코테 스터디 3일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 모 아니면 도 라는 식으로 리턴될 땐 모로 선언하고 도일 때만 바꿔주기
- 공부한 내용 본인의 언어로 정리하기
    * 코틀린은 when이 참 좋아요

```
class Solution {
    fun solution(s: String): Boolean {
        var pCount = 0
        var yCount = 0

        val lowerCaseString = s.toLowerCase()

        for (char in lowerCaseString) {
            when (char) {
                'p' -> pCount++
                'y' -> yCount++
            }
        }

        return pCount == yCount
    }
}
```

- 오늘의 회고
    * 아 회사 코드 다 때려부시고 싶다
 

### 99클럽 코테 스터디 4일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * parseInt ..... 파싱파싱
- 공부한 내용 본인의 언어로 정리하기
    * 코틀린도 같습니다...


- 오늘의 회고
    * 동시성 처리하고싶은데 디비에 바로 커넥트해서 업뎃/인서트하니까 문제가 있다아아 근데 레디스가 없어어어
    * 근데 임베디드 레디스로 어떻게든 해결해보고 싶은데
    * 용량 다이죠부일까
 
  
### 99클럽 코테 스터디 5일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 모를 땐 for문 이중 돌렸겠지...
- 공부한 내용 본인의 언어로 정리하기
```
class Solution {
   fun solution(participant: Array<String>, completion: Array<String>): String {
      participant.sort()
      completion.sort()
        
         for (i in completion.indices) {
            if (participant[i] != completion[i]) {
               return participant[i]
            }
         }
        
         return participant[participant.size - 1]
   }
}
```

- 오늘의 회고
  * array 잘 안써서 쩝



필수 해시태그: #99클럽 #코딩테스트준비 #개발자취업 #항해99 #TIL
