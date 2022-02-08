npm,npx & Typescript - Week 4

Week challenges (Tuesday) 

Find the odd int

Stop gninnipS My sdroW!


Week challenges (Wednesday)

Array.diff

Create Phone Number

Week challenges (Thursday) 

Detect Pangram

Find the missing letter

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
      
      if (arr.length === 1) {
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
    
  if (rep.length == 1){
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
