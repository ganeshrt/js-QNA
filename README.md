# js-QNA

## JS Programs

1.  highest occurring element present in array
    ``
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
