![image](https://github.com/user-attachments/assets/1da85eaf-3c44-4909-999a-9693de01efd6)# coTe
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


### 99클럽 코테 스터디 6일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 문제 이해하는게 점점 더 ...
- 공부한 내용 본인의 언어로 정리하기
```
fun solution(nums: IntArray): Int {
    val max = nums.size / 2
    val uniqueNumbers = nums.toSet()

    return if (max > uniqueNumbers.size) {
        uniqueNumbers.size
    } else {
        max
    }
}
```

- 오늘의 회고
  코틀린 됴아아


### 99클럽 코테 스터디 7일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 배열을 너무 안썼더니;;;;
- 공부한 내용 본인의 언어로 정리하기
```
class Solution {
    fun solution(arr: IntArray): IntArray {
        val result = mutableListOf<Int>()
        
        for (i in arr.indices) {
            if (i == 0 || arr[i] != arr[i - 1]) {
                result.add(arr[i])
            }
        }
        
        return result.toIntArray()
    }
}
```

- 오늘의 회고
  * 아니, 배열 리스트로 바꾸고 리스트 배열로 바꾸는게 왜이렇게 귀찮냐
 

### 99클럽 코테 스터디 8일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 스택/큐 오랜만!
- 공부한 내용 본인의 언어로 정리하기
   * 코틀린에서는 deque를 쓴다는디?
  
```
class Solution {
    fun solution(s: String): Boolean {
        val stack = ArrayDeque<Char>()
        for (item in s) {
            when (item) {
                '(' -> stack.addLast(item)
                ')' -> {
                    if (stack.isEmpty()) {
                        return false
                    } else {
                        stack.removeLast()
                    }
                }
            }
        }
        return stack.isEmpty()
    }
}
```

- 오늘의 회고
  * deque, arrayDeque 공부좀 해봐야할듯

```
import java.util.*;

class Solution {
    boolean solution(String s) {
        Stack<Character> stack = new Stack<>();
        for (char item : s.toCharArray()) {
            if (item == '(') {
                stack.push(item);
            } else {
                if (stack.isEmpty()) {
                    return false;
                } 
                
                stack.pop();
            }
        }
        
        return stack.isEmpty();
    }
}
```

### 99클럽 코테 스터디 9일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * for문 두 번이 최선인가
- 공부한 내용 본인의 언어로 정리하기
* 코틀린이면 forEach나 컬렉션 함수로 정리했을 듯

- 오늘의 회고
  * 회식해서 자세한 내용 기입 힘들다...
  * 정신 들고 다시 정리할 예정
  
### 99클럽 코테 스터디 10일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * add-offer, remove-poll 차이
- 공부한 내용 본인의 언어로 정리하기
*

- 오늘의 회고
  * 다시 정리 예정
 
### 99클럽 코테 스터디 12일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * StringBuilder / StringBuffer
- 공부한 내용 본인의 언어로 정리하기
코틀린
```

class Solution {
    fun solution(s: String): String {
        return s.toCharArray()
            .sortedArrayDescending()
            .concatToString()
    }
}
```

- 오늘의 회고
  * 난 이제 늙어서 reverse()를 안쓰고 for문 돌리는 건 못하겠다.
  * StringBuilder/StringBuffer 차이
 
### 99클럽 코테 스터디 13일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 이진-이분탐색
    *    작은 건 왼쪽 노드 하위로 큰건 오른쪽 노드 하위로
- 공부한 내용 본인의 언어로 정리하기

코틀린
```

fun searchBST(root: TreeNode?, val: Int): TreeNode? {
    var currentNode = root

    while (currentNode != null) {
        if (currentNode.val == val) {
            return currentNode
        } else if (currentNode.val < val) {
            currentNode = currentNode.right
        } else {
            currentNode = currentNode.left
        }
    }

    return null
}
```

- 오늘의 회고
  * 트리노드 처음...

### 99클럽 코테 스터디 14일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 이진-이분탐색 또....
- 공부한 내용 본인의 언어로 정리하기

코틀린
```

class Solution {
    fun isSymmetric(root: TreeNode?): Boolean {
        return root == null || symmetricChecker(root.left, root.right)
    }

    private fun symmetricChecker(left: TreeNode?, right: TreeNode?): Boolean {
        if (left == null && right == null) return true
        if (left == null || right == null || left.`val` != right.`val`) return false
        
        return symmetricChecker(left.left, right.right) && symmetricChecker(left.right, right.left)
    }
}
```

- 오늘의 회고
  * 이분탐색 좀 낯설다 근데 재밌네
 
 
### 99클럽 코테 스터디 15일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 특별히 생각나는게 없이 그냥 for문과 배열들로 해결...
- 공부한 내용 본인의 언어로 정리하기

```

class Solution {
    public int[] solution(int[] answers) {
        int[] student1 = {1,2,3,4,5};
        int[] student2 = {2,1,2,3,2,4,2,5};
        int[] student3 = {3,3,1,1,2,2,4,4,5,5};
        
        int[] score = new int[3];
        
        for (int i = 0; i < answers.length; i++) {
            if (answers[i] == student1[i%5]) {
                score[0]++;
            }
            
            if (answers[i] == student2[i%8]) {
                score[1]++;
            }
            
            if (answers[i] == student3[i%10]) {
                score[2]++;
            }
        }
        
        int maxScore = Math.max(score[0], Math.max(score[1], score[2]));
        
        List<Integer> answer = new ArrayList<>();
        
        for (int i = 0; i < 3; i++) {
            if (maxScore == score[i]) {
                answer.add(i + 1);
            }
        }
        
        return answer.stream()
                .mapToInt(Integer::intValue)
                .toArray();
    }
}
```

- 오늘의 회고
  * 배열좀 안썼으면 좋겠다
  
### 99클럽 코테 스터디 16일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 이차원 배열 기억에서 끄집어내는 데 좀 걸림
    * 하다가 너무 비효율적이어서 구글링
- 공부한 내용 본인의 언어로 정리하기

```

class Solution {
    public int solution(int[][] sizes) {
        int answer = 0;
         int temp = 0;
        int maxW = 0; int maxH = 0;
        
        for (int i = 0; i < sizes.length; i++) {
            if (sizes[i][0] < sizes[i][1]){
                temp = sizes[i][0];
                sizes[i][0] = sizes[i][1];
                sizes[i][1] = temp;
            }
        }
        
        for (int i = 0; i < sizes.length; i++) {
            maxW = Math.max(maxW, sizes[i][0]);
            maxH = Math.max(maxH, sizes[i][1]);
        }
        
        answer = maxW * maxH;
        return answer;
    }
}
```

- 오늘의 회고
  * ...후

### 99클럽 코테 스터디 17일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 바이너리 트리 
- 공부한 내용 본인의 언어로 정리하기

```

class Solution {
    public List<Integer> inorderTraversal(TreeNode root) {
    if (root == null) {
      return Collections.emptyList();
    }
    List<Integer> result = new ArrayList<>();
    travel(result, root);
    return result;
  }

  private void travel(List<Integer> result, TreeNode root) {
    if (root == null) {
      return;
    }
    travel(result, root.left);
    result.add(root.val);
    travel(result, root.right);
  }
}
```

- 오늘의 회고
  * 이건 구글링
 
### 99클럽 코테 스터디 18일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 바이너리 트리 언제까지,,,
- 공부한 내용 본인의 언어로 정리하기

```

public class Solution {

  private TreeNode head;
  private TreeNode current;

  public TreeNode increasingBST(TreeNode root) {
    traverse(root);
    return head;
  }

  private void traverse(TreeNode node) {
    if (node == null) {
      return;
    }
    traverse(node.left);
    TreeNode n = new TreeNode(node.val); 
    if (head == null) {
      head = n;
      current = n;
    } else {
      current.right = n;
      current = current.right;
    }
    traverse(node.right); 
  }
}
```

- 오늘의 회고
  * 구글링2
 

### 99클럽 코테 스터디 19일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * greedy algorithm
- 공부한 내용 본인의 언어로 정리하기

```

import java.util.*;

class Solution {
    public int solution(int k, int m, int[] score) {
        int answer = 0;
        
        Arrays.sort(score);
        
        for (int i = score.length - m; i >= 0; i -= m) {
            answer += m * (score[i]);
        }
        return answer;
    }
}
```

- 오늘의 회고


### 99클럽 코테 스터디 20일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * greedy algorithm
- 공부한 내용 본인의 언어로 정리하기

```

import java.util.HashSet;
import java.util.Set;

class Solution {
    public int solution(int n, int[] lost, int[] reserve) {
        Set<Integer> reserveSet = new HashSet<>();
        Set<Integer> lostSet = new HashSet<>();
        
        for (int i : reserve) {
            reserveSet.add(i);
        }

        for (int i : lost) {
            if (!reserveSet.remove(i)) {
                lostSet.add(i);
            }
        }

        for (Integer i : reserveSet) {
            if (lostSet.contains(i - 1)) {
                lostSet.remove(i - 1);
            } else if (lostSet.contains(i + 1)) {
                lostSet.remove(i + 1);
            }
        }

        return n - lostSet.size();
    }
}
```

- 오늘의 회고
  * 배열 변환할 때 번거로움...중복 제거는 list보다 set이 낫겠구나

### 99클럽 코테 스터디 21일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 파스칼
- 공부한 내용 본인의 언어로 정리하기

```

class Solution {
    public List<List<Integer>> generate(int numRows) {
        // 0번째 배열을 제외하고는 모두 1을 양쪽에 가지고 있음
        List<List<Integer>> answer = new ArrayList<>(numRows);

        for (int i = 0; i < numRows; i++) {
            List<Integer> innerList = new ArrayList<>(i + 1);
            
            if (i == 0) {
                innerList.add(1);
            } else {
                for (int j = 0; j <= answer.size(); j++) {
                    List<Integer> beforeList = answer.get(i - 1);

                    if (j == 0 || j == answer.size()) {
                        innerList.add(1);
                    } else {
                        innerList.add(beforeList.get(j - 1) + beforeList.get(j));
                    }
                }
            }

            answer.add(innerList);
        }

        return answer;
    }
}
```

- 오늘의 회고
  * 이렇게 해도 되나 뭔가 속도 이슈가...

### 99클럽 코테 스터디 22일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * array partition
- 공부한 내용 본인의 언어로 정리하기

```

class Solution {
    public int arrayPairSum(int[] nums) {
        Arrays.sort(nums);
        int result = 0;

        for (int num = 0; num < nums.length; num += 2){
            result += nums[num];
        }
        
        return result;
    }
}
```

- 오늘의 회고
  * 런타임 속도가....;;

### 99클럽 코테 스터디 24일차 TIL + 오늘의 학습 키워드
- 오늘의 학습 키워드
    * 이차원 배열 
- 공부한 내용 본인의 언어로 정리하기

```

class Solution {
    public int findCenter(int[][] edges) {
        int a = edges[0][0], b = edges[0][1];
        int c = edges[1][0], d = edges[1][1];
        return a == c || a == d ? a : b;
    }
}
```

- 오늘의 회고
  * 중복값 찾기
필수 해시태그: #99클럽 #코딩테스트준비 #개발자취업 #항해99 #TIL
