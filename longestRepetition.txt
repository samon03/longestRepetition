function longestRepetition (str) {
    let longest = 0;
    let length = 1;
    let strLong = '';
     let longer = '';
    for (let i = 0; i < str.length - 1; i++) {
        if (str.charAt(i) === str.charAt(i + 1)) {
            ++length;
            if (length > longest) {
                longest = length;
                strLong = str.charAt(i);
            }
        } else {
            length = 1;
        }
    }
    if (length > longest) {
        longest = length;
    }

    for(let j = 0; j < longest;  j++) {
      longer += strLong;
    }

    return longer;
   

}

console.log(longestRepetition('aanyyeeeddk'));