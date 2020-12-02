## 손코딩 연습
https://programmers.co.kr/learn/challenges

- 여기에 풀었던 문제가 대부분이지만 다시한번 손으로 풀어보려고 한다. 그리고 [손코딩 공부하면서 참고한 자료](https://imasoftwareengineer.tistory.com/66) 이제 1월부터는 이렇게 코딩하는 연습을 해야겠다. 

- [시간복잡도 예상하기](https://allo-ew.tistory.com/69) 1,000,000 -> n, nlogn / 10,000 -> n의 제곱
  


1. [문제](https://programmers.co.kr/learn/courses/30/lessons/42576)
- 풀이
```
#include <string>
#include <vector>
#include <algorithm>

using namespace std;

string solution(vector<string> participant, vector<string> completion) {
    string answer = "";
    
    sort(participant.begin(), participant.end());
    sort(completion.begin(), completion.end());
    
    for(int i = 0; i < completion.size(); i++){
        if(participant[i] != completion[i]){
            return participant[i];
        }
    }
    
    answer = participant.back();
    
    return answer;
}
```
- 손코딩
<img src="1.jpeg" width=400>


2. [문제](https://programmers.co.kr/learn/courses/30/lessons/42577) 
- 풀이: 
```
#include <string>
#include <vector>
#include <algorithm>
#include <iostream>

using namespace std;

bool solution(vector<string> phone_book) {
    bool answer = true;
    sort(phone_book.begin(), phone_book.end());
    
    for(int i = 0; i < phone_book.size() - 1; i++){
        // cout << phone_book[i] << " ";
        if(phone_book[i].size() <= phone_book[i+1].size()){
            if(phone_book[i] == phone_book[i+1].substr(0, phone_book[i].size())){
                return false;
            }  
        }
    }
    return answer;
}
```

- 손코딩:
<img src="2.jpeg" width=400>


3. [문제](https://programmers.co.kr/learn/courses/30/lessons/42578) 
- 풀이: 
```
#include <string>
#include <vector>
#include <map>

using namespace std;

int solution(vector<vector<string>> clothes) {
    int answer = 1;
    vector<string> v;
    map<string, int> m;
    
    for(int i = 0; i < clothes.size(); i++){
        if(m.count(clothes[i][1]) == 0){
            v.push_back(clothes[i][1]);
            m[clothes[i][1]] = 1;
        } else {
            m[clothes[i][1]]++;
        }
    }
    
    for(int i = 0; i < v.size(); i++){
        answer *= (m[v[i]] + 1);
    }
    answer -= 1;
    
    return answer;
}
```

- 손코딩:
<img src="3.jpeg" width=400>


1. [문제]() 
- 풀이: 
- 손코딩:



5. [문제]() 
- 풀이: 
- 손코딩: