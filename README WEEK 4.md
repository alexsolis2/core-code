                                                                 npm,npx & Typescript - Week 4

Week challenges (Tuesday) 

Find the odd int

function comparar ( a, b ){ return a - b; }


function findOdd(A) {

  A = A.sort(comparar);
  
  console.log(A)
  
  var cantidad = 1;
  
  var comparar = A[0];
  
  A = A.slice(1);
  
  for (let i = 0; i<A.length; i++)
    {
    
      if (A[i] == comparar)
      
        {
          cantidad = cantidad + 1;
        }
        
      else
      {
      
        if (cantidad % 2 != 0) 
        
        {
         console.log(comparar);
         
         return comparar
        }
        
        else
          {
          
            comparar = A[i]
            
            cantidad = 1
          
          }
      }
      
    }
    
  console.log(comparar)
  
  return comparar
}

Stop gninnipS My sdroW!

function inversestring(string)

{

  var largo = string.length-1;
  
  var retorno = "";

  while (largo !== -1)
  
    {
    
    retorno = retorno + string[largo]; 
    largo = largo - 1
    
    }
    
  return (retorno)
}

function spinWords(string)
{

  var retorno = ""
  
  string = string.split(" ");
  
  for (let i = 0; i<string.length; i++)
    {
    
      if (string[i].length >= 5)
      
      {
       var aux = inversestring(string[i]);
       retorno = retorno + aux + " "
      }
      
      else
      {
        retorno = retorno + string[i]+" ";
      }
        
    }
    
  console.log(retorno.slice(0,-1))
  return (retorno.slice(0,-1))
  
}


Week challenges (Wednesday)


Array.diff

function arrayDiff(a, b) 
  {
     if (a.length == 0){return []}
  
      else if (b.length == 0){return a}
  
      else
      {
       var retorno = [];
       
       for (let i = 0; i < a.length ; i++)
       
       {
       
       if (b.includes(a[i])===false){retorno.push(a[i]);}
       
       }
  
  }
  
  return retorno;
}


Create Phone Number

function createPhoneNumber(numbers)

{

  var p = numbers[0].toString()+numbers[1]+numbers[2]

  var m = numbers[3].toString()+numbers[4]+numbers[5]
  
  var f = numbers[6].toString()+numbers[7]+numbers[8]+numbers[9]
  
  var retorno = "";
  
  retorno = retorno+"("+p+")"+" "+m+"-"+f
  
  console.log (retorno);
  
  return retorno;
  
  
}

Week challenges (Thursday) 


Detect Pangram

function isPangram(string)

  {
  
  string = string.toLowerCase()
  
  var alfa = "abcdefghijklmnopqrstuvwxyz"
  
  for (let i = 0; i<alfa.length; i++)
    
    {
      
      if (string.includes(alfa[i]) === false)
        
        {
        
         console.log(alfa[i]);
         
         console.log(false);
         
         return false
        
        }
     }
     
  console.log (true)
  
  return (true);

}

Find the missing letter

function arrayDiff(a, b) 
{
  
  if (a.length === 0){return []}
  
  else if (b.length === 0){return a}
  
  else
    {
  
    var retorno = [];
    
    for (let i = 0; i < a.length ; i++)
      
      {
      
      if (b.includes(a[i])===false){retorno.push(a[i]);}
      
      }
    
    }
    
  return retorno;
}

function findMissingLetter(array)

  {
  
  var alfami = "abcdefghijklmnopqrstuvwxyz"
  
  alfami = [...alfami];
  
  console.log(alfami)
  
  var alfama = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
  
  alfama = [...alfama];
  
  array = array.join().replace(/,/g,"").toString();
  
  if (array[0] === array[0].toLowerCase())
    
    {
     
     console.log("minusculas");
     
     console.log(alfami.indexOf(array[0]))
     
     var inicio = alfami.indexOf(array[0])
     
     var fin = alfami.indexOf(array[array.length-1])+1
     
     console.log(alfami.indexOf(array[array.length-1]))
     
     var aux = alfami.slice(inicio,fin);
     
     var res = arrayDiff(aux,array);
     
     console.log(res[0])
     
     return res[0]
     
    }
    
  else
  
    {
    
    console.log("mayusculas")
    
    console.log(alfama.indexOf(array[0]))
    
    var inicio = alfama.indexOf(array[0])
    
    var fin = alfama.indexOf(array[array.length-1])+1
    
    console.log(alfama.indexOf(array[array.length-1]))
    
    var aux = alfama.slice(inicio,fin);
    
    var res = arrayDiff(aux,array);
    
    console.log(res[0])
    
    return res[0]
  
    } 

}

Find the unique number


function findUniq(arr) {

  var rep = []
  
  arr = arr.sort();
  
  console.log("Primer Array: "+arr)
  
  while(arr.length !== 0)
  
    {
      var actual = arr[0];
      
      var counter = 1;
      
      arr = arr.slice(1)
      
      if (arr.length === 1) 
      {
      
        console.log("unico: "+arr[0]);
      
        return arr[0];
        
      }
      
      else if (arr.includes(actual) === false && rep.includes(actual) === false)
        {
          console.log("unico: "+actual)
          
          return (actual)
        }
        
     else 
       {
       
         if (arr.includes(actual) && rep.includes(actual) === false)
         
         {
         
         rep.push(actual)
         
         console.log("Repetidos: "+rep)
         
         actual = arr[0]
         
         console.log("Nuevo actual: "+actual)
         
         arr = arr.slice(1)
         
         console.log("Nuevo: "+arr)
         
         }
       }
      
    }
    
  if (rep.length == 1)
  {
    console.log(NaN);
  
    return NaN;
    
  }
}

Reverse or rotate?

function cubessum(string){

  var sum = 0;
  
  for (let i = 0; i<string.length; i++)
    {
      sum = sum + Math.pow((parseInt(string[i],10)),3);
    }
    
  console.log(sum);
  
  if (sum%2===0)
    {
      string = string.split('').reverse().join('');
    }
    
  else
    {
      string = string + string[0]
      
      string = string.slice(1)
    }
    
  console.log(string)
  
  return string
}


function revrot(str, sz) {

  if (str.length === 0 || sz <= 0 || sz > str.length) 
  
  {
    console.log ("");
    
    return "";
  }
  
  var retorno = ""
  
  while (str.length!==0)
  
  {
    console.log(str.slice(0,sz));
    
    if (str.slice(0,sz).length >= sz)
    
    {
      
      retorno = retorno + cubessum(str.slice(0,sz))
    
      str = str.slice(sz);
    
    }
  }
  
  console.log("retorno: "+retorno)
  
  return (retorno);
}

What's Your Poison?

function find(rats) {

  var res = 0;
  
  for (let i = 0; i<rats.length; i++)
  
  {
  
   res = res + Math.pow(2,rats[i])
  
  }
  
  return res
  
}
