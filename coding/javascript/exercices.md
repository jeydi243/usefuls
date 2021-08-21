# Exercices
## Question 1 : Count the number of Duplicates
Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.
  **Example**
  - "abcde" -> 0 # no characters repeats more than once
  - "aabbcde" -> 2 # 'a' and 'b'
  - "aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)
  - "indivisibility" -> 1 # 'i' occurs six times
  - "Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice
  - "aA11" -> 2 # 'a' and '1'
  - "ABBA" -> 2 # 'A' and 'B' each occur twice 

### Solution
```javascript
function duplicateCount(text){
  return getRepeatedChars(text.toLowerCase()).length
}

const getRepeatedChars = (str) => {
 	const chars = {};
    for (const char of str) {
        chars[char] = (chars[char] || 0) + 1;
    }
    return Object.entries(chars).filter(char => char[1] > 1).map(char => char[0]);
}

```
## Question 2 
On vous donne un tableau (qui aura une longueur d'au moins 3, mais qui peut être très grand) contenant des entiers. Le tableau est soit entièrement composé d'entiers impairs, soit entièrement composé d'entiers pairs, à l'exception d'un seul entier N. Écrivez une méthode qui prend le tableau comme argument et renvoie ce N "etranger".

**Exemples** 
[2, 4, 0, 100, 4, 11, 2602, 36]
Doit retourner: 11 (nombre impair)

[160, 3, 1719, 19, 11, 13, -21]
Doit retourner: 160 (nombre pair)
### Solution
```javascript
function findOutlier(integers){
  var result = []
  for(i=0;i<integers.length;i++){
    result.push(isOdd(integers[i]) ? true:false)
  }
  var odd = result.filter(x => x == true).length
  var even = result.filter(x => x == false).length
  if(odd < even) return integers.find(x => x%2 ==0)
  return integers.find(x => x%2 !=0)
}
function isOdd(x){ return x%2 == 0}
```
#### Test
`describe("Tests", () => {
  it("test if", () => {
    Test.assertEquals(findOutlier([0, 1, 2]), 1)
    Test.assertEquals(findOutlier([1, 2, 3]), 2)
    Test.assertEquals(findOutlier([2,6,8,10,3]), 3)
    Test.assertEquals(findOutlier([0,0,3,0,0]), 3)
    Test.assertEquals(findOutlier([1,1,0,1,1]), 0)
  });
});`