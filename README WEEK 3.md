Javascript - Week 3

Week challenges (Monday) 

https://www.codewars.com/kata/5266876b8f4bf2da9b000362

https://www.codewars.com/kata/526571aae218b8ee490006f4

Week challenges (Tuesday) 

https://www.codewars.com/kata/55c45be3b2079eccff00010f

https://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1

https://www.codewars.com/kata/520b9d2ad5c005041100000f

Week challenges (Wednesday)

https://www.codewars.com/kata/55c45be3b2079eccff00010f

https://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1

https://www.codewars.com/kata/520b9d2ad5c005041100000f

Week challenges (Thursday) 

https://www.codewars.com/kata/57ea70aa5500adfe8a000110

https://www.codewars.com/kata/5848565e273af816fb000449

function list(names){
  var retorno = "";
  
  if (names.length === 0){return "";}
  
  if (names.length <= 2)
    {
      if (names.length == 1){return names[0].name;}
      
      else
        return names[0].name +" "+"&"+" "+names[1].name;
    }
  else
  
    while (names.length !== 1){
    
      retorno = retorno + names[0].name+","+" ";
      
      names = names.slice(1);
  }
  
  retorno = retorno.slice(0,-2);
  
  retorno = retorno + " "+"&"+" "+names[0].name;
  
  return (retorno);
}


