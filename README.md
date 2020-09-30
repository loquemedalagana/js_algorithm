# 자바스크립트 알고리즘 문제풀이
<ul>
    <li>백준 문제는 입출력이 간단한거 위주로 올립니다.</li>
    <li>유용한 라이브러리나 boilarplate 코드 공유합니다.</li>
</ul>

<hr/>

## js 문자열 체크

``` javascript
const numPattern = /[0-9]/; //숫자 있는지 체크
const alphabetPattern = /[a-zA-Z]/; //알파벳 있는지 체크
const specialCharacterPattern = /[~!@#$%^&*()_+|<>?:{}]/; //특수문자 체크

const checkSpace = str => { //공백 체크
    return str.search(/\s/) !== -1 ? true : false;
};
```

## JS 정수 정렬

``` javascript
arr.sort((first, second) => first-second); //내림차순은 반대로
```

## js permutation

``` javascript
const permutation = arr => {
    return arr.reduce((list, element) => {
        console.log(list, element);
        let newList = [];
        list.forEach(seq => {
            for(let i = seq.length; i>=0; i--){
                let newSeq = [].concat(seq);
                newSeq.splice(i, 0, element);
                newList.push(newSeq);
            }
        })
        return newList;
    }, [[]]);
}

```

## js queue
``` javascript
function Queue() {
    this.elements = [];
    Queue.prototype.push = element => {
        this.elements.push(element);
    }    
    Queue.prototype.pop = () => this.elements.shift();
    Queue.prototype.empty = () => this.elements.length === 0;
    Queue.prototype.front = () => !this.empty() ? this.elements[0] : undefined;
    Queue.prototype.size = () => this.elements.length;    
}
```

## js pair
``` javascript
function Pair (first, second) {
    this.first = first;
    this.second = second;
}
```

## 참고 블로그
https://dev-muko.com/entry/1%EC%B0%A8%EC%9B%90-%EB%B0%B0%EC%97%B4-%ED%8E%B81-Nodejs%EB%A1%9C-%EB%B0%B1%EC%A4%80BOJ-%EB%8B%A8%EA%B3%84%EB%B3%84%EB%A1%9C-%ED%92%80%EC%96%B4%EB%B3%B4%EA%B8%B0%EB%A5%BC-%ED%92%80%EC%96%B4%EB%B3%B4%EB%8B%A4?category=907653