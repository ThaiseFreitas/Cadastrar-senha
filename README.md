function validatePassword (senha){

    if(senha. length< 8){
        return false;
    }
    if(!hasLetter(senha)){
        return false;
    }

    if(!hasNumber(senha)){
        return false;
    }

    if(!hasSpecialCharactere(senha)){
        return false;
    }
    return true;
}


function hasLetter(senha){

    for(let i =0; i < senha.length; i++){
        if((senha[i] >= 'a' && senha[i]<='z') || (senha[i] >= 'A' && senha[i]<='Z')) {
            
            return true;
            

        }
    }

    return false;
}

function hasNumber(senha){

    for(let i =0; i < senha.length; i++){
        if(senha[i] >= '0') {
            
            return true;
            

        }
    }

    return false;
}

function hasSpecialCharactere(senha){

    for(let i =0; i < senha.length; i++){
        if(senha[i]==='@' || senha[i]==='#' || senha[i]==='&') {
            
            return true;

        }
    }

    return false;
}



console.log(validatePassword("amrca154682"));

console.log(validatePassword("amerca1@"));

console.log(validatePassword("amerca"));

console.log(validatePassword("1234"));

console.log(validatePassword("@#$%"));
   
    

    
 
