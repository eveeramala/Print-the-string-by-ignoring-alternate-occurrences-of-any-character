# Print-the-string-by-ignoring-alternate-occurrences-of-any-character
Given a string of both uppercase and lowercase alphabets, the task is to print the string with alternate occurrences of any character dropped(including space and consider upper and lowercase as same).  
Examples:  
Input : It is a long day Dear. 
Output : It sa longdy ear. 
Print first I and then ignore next i. Similarly print first space then  ignore next space.

    var alternateStr = function(S) {

    let map = {}, res = '';
    
    S = S.toLowerCase();
    
    for(let i = 0;i < S.length; i++) {
    
        if(map[S[i]] === undefined) {
        
            res += S[i];
            
            map[S[i]] = 1;
            
        }
        
        else {
        
            map[S[i]] = undefined;
            
        }
    }
    
    return res;
    
    };
