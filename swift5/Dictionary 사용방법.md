### 딕셔너리 Dictionary

+ 키-값으로 구성된 데이터 타입 자바:Map JS:Key-Value객체
+ JSON
+ ["key1": value2, "key2": value2]

### 순서가 없는 데이터 구조
~~~ 
let myDic: [String: String] = ["key1": "value1", "key2": "value2"]
print( myDic )

//요소에 접근하는 법
print( myDic["key1"]! )
print( myDic["key2"]! )

var nameDic = ["name1": "홍길동", "name2": "변사또", "name3": "순향이"]
//새로운 요소를 추가
nameDic["name6"] = "이몽룡"
print( nameDic )

//Dic을 순환하기
for (key, value) in nameDic {
    print( key )
    print( value )
}

//요소 삭제
nameDic.removeValue(forKey: "name2")
print( nameDic )

//갯수
nameDic.count

//NS계열 : NSDictionary(수정불가), NSMutableDictionary 변경가능(추가,삭제)
//Swift계열 : Dictionary(var, let)
~~~

### 집합 Set
~~~
//요소의 중복을 허용하지 않는 데이터 타입 : 자바 set(hashset)
var mySet: Set<Int> = []
mySet.insert( 10 )
mySet.insert( 20 )
mySet.insert( 30 )
print( mySet )
let result = mySet.insert( 30 ) //데이타를 중복해서 넣을때, 무시됨.
print( result )
print( mySet )

mySet.isEmpty
mySet.contains( 20 )

//집합 연산
var mySet2: Set<Int> = [10, 20, 30]
var mySet3: Set<Int> = [30, 40, 50]
//합집합 A + B
var setSum = mySet2.union( mySet3 )
print( setSum )
//교집합 A ^ B
var setCross = mySet2.intersection( mySet3 )
print( setCross )
//차집합 A - B
var setSub = mySet2.subtracting( mySet3 )
print( setSub )

//NS계열: NSSet 변경불가 NSMutableSet 변경가능
//Swift계열 : Set( let, var )
~~~
