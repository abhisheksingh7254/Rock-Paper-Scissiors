<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Functions</title>
  <style>
    body{background: #6eb2e3;}
  </style>
</head>
<body>
    <div class="container">
      <button
        onclick="
        playGame('Rock');
        "
        >
          Rock
        </button>
        <!--Part 2-->
        <button
          onclick="
            playGame('Paper');
          "
          >
        Paper
      </button>
      <button
        onclick="playGame('Scissiors');">
        Scissiors
      </button>
  </div>
    <script>
      function playGame(playerMove){
        computerNum=computerMove();
        let result='';

        if(playerMove==='Scissiors'){

            if(computerNum==='Rock'){
              result='You Loose';
            }else if(computerNum==='Paper') {
              result= 'You win';
            }else if(computerNum==='Scissiors') {
              result='Match Ties';
            }else{
            result='Nothing';
            }
            alert(`computer selected ${computerNum}  and You selected ${playerMove}.so ${result}`);

        }else if(playerMove==='Paper'){
          
            if(computerNum==='Rock'){
              result='Hurrey!!...You Win';
            }else if(computerNum==='Paper') {
              result= 'Match Ties';
            }else if(computerNum==='Scissiors'){
              result='You Loose';
            }else{
              result='Nothing';
            }
              alert(`Hello2 computer selected ${computerNum} and You selected ${playerMove}.so ${result}`);
            /*alert(`Computer choose ${computerNum},You choose Paper.\n${result});*/
        }else if(playerMove==='Rock'){
           
            if(computerNum==='Rock'){
              result='Match Ties';
              }else if(computerNum==='Paper') {
              result= 'You Loose';
              }else if(computerNum==='Scissiors'){
              result='Hurrey!!...You Win';
              }else{
              result='Nothing';
              }
              alert(`Hello1 computer selected ${computerNum} and You selected ${playerMove}.so ${result}`);
              /*alert(`Computer choose ${computerNum}, You choose Rock,\n${result} `);*/
           }
        }
        
      function computerMove(){
        const randomNum=Math.random();
        <!-- console.log(randomNum); -->
        let computerNum='';
        if(randomNum>0 && randomNum<=1/3){
        computerNum='Rock';
        }else if(randomNum>1/3 && randomNum<=2/3){
        computerNum='Paper';
        }else if(randomNum>2/3 && randomNum<1){
        computerNum= 'Scissiors';
        }
        return computerNum;
      }
    </script>
</body>
</html>
