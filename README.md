# js-QNA

## JS Programs

1.  highest occurring element present in array

        function mostFrequent(arr) {
        const res = arr.sort((a, b) => {
            return arr.filter(v => v === a).length - arr.filter(v => v === b).length
        }).pop()
        console.log(res)
        //         return res;
        }
        mostFrequent([2, 'b', 'a', 'c', 1, 'a', 3, 'a', 4, 4, 2, 3]);

2.  Remove Duplicate from Array

        const arr=[1,6,3,4,2,4,1,];
        const newArr = [ ...new Set(...arr)];

3.Print pattern Pyramid

        const diamond = (n) => {
         let str = "";
         for (let i = 0; i <= n; i++) {
             for (let j = 1; j <= n - i; j++) {
                 str += " ";
             }
        // printing star
             for (let k = 0; k < 2 * i - 1; k++) {
                str += "*";
         }
         str += '\n'
          }
    console.log(str);
        }
        diamond(5);

4.find out how many times 1 present in given array [1, 0, 0, 0, 0, 1, 0, 1] without using any conditional operator;

        let arr = [1, 0, 0, 0, 0, 1, 0, 1]; //given
        let ob = {
        1: 0,
        0: 0
        }
        arr.map((item) => {
        ob[item]++;
        })
        console.log(ob["1"]); // output 3

5.  remove duplicates and find the sum of all elements

        const arr=[1,6,3,4,2,4,1,];
        const newArr = [ ...new Set(...arr)];
        let sum=0;
        newArr.map((item) => { sum+=item});
        console.log(sum);

6.write program for

Input : {emp1:{ name:"ganesh",...}....}
output :
[ { id: 'emp1', name: 'ganesh', empId: '123' }],

        const res =[];
        const objToArr =(obj) =>{
        let newObj ={};
        for (const [key, value] of Object.entries(obj )) {
        let newObj ={};
        newObj["id"] =key;

        if(typeof value ==='object'){
            for (const [k, v] of Object.entries(value))
            {
                newObj[k] =v;
            }
        }
        res.push(newObj);
        }
        console.log(res);
        }
        objToArr({emp1:{name:"ganesh",empId:"123"}});

7.  reverse the "Hello world" to "olleH dlrow";

        const str = "Hello world" //given input string
        const newStr =str.split("").reverse().join("");
        const reverse = newStr.split(" ").reverse().join(" ");
        console.log(reverse);

8.Given two strings, return true if they are anagrams of one another;

    var firstWord = "Mary";
    var secondWord = "Army";

    isAnagram(firstWord, secondWord); // true

    function isAnagram(first, second) {
    // For case insensitivity, change both words to lowercase.
    var a = first.toLowerCase();
    var b = second.toLowerCase();

    // Sort the strings, and join the resulting array to a string. Compare the results
    a = a.split("").sort().join("");
    b = b.split("").sort().join("");

    return a === b;
    }
