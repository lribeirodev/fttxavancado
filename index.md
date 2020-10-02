<html>
<head>
 <title>
   Suporte Avançado
 </title>
 
 <style>

span{
    font-weight: bold; 
    color: white;  
    display: block;
    margin: 10px auto; 
    padding: 10px 0px 10px 5px;
}

 </style>

</head>

 <body>
   

    <p id="dgoi-c"></p>

   <script>
     
     alert("Bem vindo ao Suporte Avançado FTTX\nCriador Lucas Ribeiro");
     
     function menu(){
       var op=prompt("Selecione uma opção para prosseguir\n[1] Calculadora DGOI-C\n[X] Calcular DGOI Splitter\n[3] Calcular DGOI PRUMADA 6\n[4] Calcular Lateral Fusionada\n[5] Contato Criador\n[0] Para finalizar o suporte");
      
    if(op==1){
       dgoic();
     }else if(op==2){
       dgoicSplitter();
     }else if(op==3){
       dgoi6Prumada();
     }else if(op==4){
       lateralFusionada();
     }else if(op==5){
       alert("Criador: Lucas Ribeiro\nWhatsapp: (11) 94131-4539");
       menu();
     }else if(op==0){
         sair();
     }else {
         menu();
     }
     
     }
     
     menu();
    
     function dgoicSplitter(){
       alert("Esta função ainda esta em desenvolvimento");
       menu();
     }
    
     function lateralFusionada(){
      
      alert("AVISO: NA LATERAL FUSIONADA PROCURE A CAIXA 1 E A SUA PRIMEIRA SECUNDÁRIA");
      
      var s1 = prompt("DIGITE A SECUNDARIA DO SEU PDA");
      var s2 = prompt("DIGITE A PRIMEIRA SECUNDARIA DA CAIXA UM");
      
       var coresTubo = ["", "VERDE","AMARELO"
        ,"BRANCO","AZUL","VERMELHO","VIOLETA"];
      
      var respTubo, respFibra;
      
      var o =  +s1 - (+s2 - 1);
      
      var indiceFibra;
     
      if(o >= 1 && o < 1+6){
        respTubo = coresTubo[1];
        respFibra = coresTubo[o];
        
      }else if(o >= 7 && o < 7+6){
        respTubo = coresTubo[2];
        indiceFibra = o-6;
        respFibra = coresTubo[indiceFibra];
        
      }else if(o >= 13 && o < 13+6){
        respTubo = coresTubo[3];
        indiceFibra=o-12;
        respFibra = coresTubo[indiceFibra];
        
      }else if(o >= 19 && o < 19+6){
        respTubo = coresTubo[4];
        indiceFibra=o-18;
        respFibra = coresTubo[indiceFibra];
        
      }else if(o >= 25 && o < 25+6){
        respTubo = coresTubo[5];
        indiceFibra=o-24;
        respFibra = coresTubo[indiceFibra];
      }
      
      alert("Cor do Tubo: " + respTubo + "\nCor da Fibra: " + respFibra);
      
      menu();
      
     }
     
     function dgoi4Prumada(){
       
      alert("Padrão para Prumada 4 Fibras por Tubo");
      
      var o = prompt("Digite a numeração da Prumada para saber \n a cor da fibra e do tubo?");
      
      var caixa = prompt("Informe a Caixa da Prumada Próximo ao andar do Cliente");
     
      var coresTubo = ["", "VERDE","AMARELO"
        ,"BRANCO","AZUL","VERMELHO","VIOLETA"
        ,"MARROM", "ROSA"];
   
      var coresFibra = ["", "VERDE", "AMARELO", "BRANCO", "AZUL"];
   
       var respTubo, respFibra;
   
   
      if(caixa==1){
        
        if(o >= 1 && o < 1+5){
          respTubo = coresTubo[1];
          respFibra = coresFibra[o];
        }else if(o >= 5 && o < 5+5){
          respTubo = coresTubo[2];
          respFibra = coresFibra[o-4];
        }
        
      }else if(caixa==2){
        
        if(o >= 1 && o < 1+5){
          respTubo = coresTubo[3];
          respFibra = coresFibra[o];
        }else if(o >= 5 && o < 5+5){
          respTubo = coresTubo[4];
          respFibra = coresFibra[o-4];
        }
        
      }else if(caixa==3){
        
        if(o >= 1 && o < 1+5){
          respTubo = coresTubo[5];
          respFibra = coresFibra[o];
        }else if(o >= 5 && o < 5+5){
          respTubo = coresTubo[6];
          respFibra = coresFibra[o-4];
        }
        
      }else if(caixa==4){

        if(o >= 1 && o < 1+5){
          respTubo = coresTubo[7];
          respFibra = coresFibra[o];
        }else if(o >= 5 && o < 5+5){
          respTubo = coresTubo[8];
          respFibra = coresFibra[o-4];
        }

      }
        
        alert("CAIXA: " + caixa + "\nCOR TUBO: " + respTubo + "\nCOR FIBRA: " + respFibra + "\nSECUNDÁRIA: " + o);
        
        
     }
     
    function dgoi6Prumada(){
        alert("Padrão para Prumada 6 Fibras por Tubo");
        
        var mode = prompt("Modo [1] Numeração maior que 48\nModo [2] Numeração menor que 48");
     
        var opt = prompt("Digite a numeração da Prumada para saber \n a cor da fibra e do tubo?");

        var NumeracaoCaboRise = [
            [0,0],
            [1,6],
            [7,12],
            [13,18],
            [19,24],
            [25,30],
            [31,36],
            [37,42],
            [43,48]
        ];

        var coresTuboRise = ["", "VERDE","AMARELO"
        ,"BRANCO","AZUL","VERMELHO","VIOLETA","MARROM","ROSA"];

        var coresRiseFibra = ["", "VIOLETA", "VERMELHO", "AZUL", "BRANCA", "AMARELA", "VERDE"];

        var respTubo, respFibra, cabo, bandeja, caixa;
        
        function validarCorTubo(){
            
            var o = opt;

            if(mode==1){
            
            cabo = 1;
            caixa = 4;
            
            if(o >= 49 && o <= 96){
                o = o - 48;
                cabo = 2;
                caixa = 8;
            }else if(o >= 97 && o <= 144){
               o = o - 96;
               cabo = 3;
               caixa = 12;
               
            }
            
            }
            
            
            if(mode==2){

            cabo = prompt("Qual cabo esta marcando na caixa?");

            if(cabo==2){
                caixa=8;
            }else if(cabo==3){
                caixa=12;
            }
           
                      }
            
            

            if(o >= 1 && o < 1+6){
                respTubo = coresTuboRise[1];
                bandeja = 1;
                caixa -=3;
            }else if(o >= 7 && o < 7+6){
                respTubo = coresTuboRise[2];
                bandeja = 1;
                caixa-=3;
            }else if(o >= 13 && o < 13+6){
                respTubo = coresTuboRise[3]
                bandeja = 2;
                caixa-=2
            }else if(o >= 19 && o < 19+6){
                respTubo = coresTuboRise[4]
                bandeja = 2;
                caixa-=2;
            }else if(o >= 25 && o < 25+6){
                respTubo = coresTuboRise[5]
                bandeja =3
                caixa-=1;
            }else if(o >= 31 && o < 31+6){
                respTubo = coresTuboRise[6]
                bandeja = 3;
                caixa-=1;
            }else if(o >= 37 && o < 37+6){
                respTubo = coresTuboRise[7]
                bandeja = 4;
            }else if(o >= 43 && o < 43+6){
                respTubo = coresTuboRise[8]
                bandeja = 4;
            }
                        
        }

      function validarCorFibra(){
            var o = opt;
            
            if(o >= 49 && o <= 96){
                o = o - 48;
            }else if(o >= 97 && o <= 144){
               o = o - 96;
            }
            
            var x = 0;
            
            if(o >= 1 && o < 1+6){
                x = 1+6 - o;
            }else if(o >= 7 && o < 7+6){
                x = 7+6 - o;
            }else if(o >= 13 && o < 13+6){
                x = 13+6 - o;
            }else if(o >= 19 && o < 19+6){
                x = 19+6 - o;
            }else if(o >= 25 && o < 25+6){
                x = 25+6 - o;
            }else if(o >= 31 && o < 31+6){
                x = 31+6 - o;
            }else if(o >= 37 && o < 37+6){
                x = 37+6 - o;
            }else if(o >= 43 && o < 43+6){
                x = 43+6 - o;
            } 
            
            o = x;
            
            switch(o){
              case 1: respFibra = coresRiseFibra[1]; break;
                case 2: respFibra = coresRiseFibra[2]; break;
                case 3: respFibra = coresRiseFibra[3]; break;
                case 4: respFibra = coresRiseFibra[4]; break;
                case 5: respFibra = coresRiseFibra[5]; break;
                case 6: respFibra = coresRiseFibra[6]; break;
            }
            
      }

      validarCorTubo();
      validarCorFibra();
      
        alert("CABO: " + cabo + "\nTUBO: " + respTubo + "\nCOR DA FIBRA: " 
        + respFibra + "\nBANDEJA DGOI: "+ bandeja + "\nCAIXA N°:" + caixa);
      
      
      
      menu();
    }
    
    function dgoic(){
    alert("Faça a leitura da tampa e insira os dados no programa");
    
    var cores = ['<span style="background-color: green; "> VERDE ' 
        ,'<span style="background-color: yellow; color: black;"> AMARELA '
        ,' <span style="background-color: white; color: black; border: 1px solid black;"> BRANCA '
        ,' <span style="background-color: blue; color: white;"> AZUL '
        , ' <span style="background-color: red; color: black;"> VERMELHO'
        , '<span style="background-color: purple; color: white;"> VIOLETA'
        , '<span style="background-color: brown; color: white;"> MARROM'
        , '<span style="background-color: pink; color: black;"> ROSA'
        , '<span style="background-color: black; color: white;"> PRETO'
        , '<span style="background-color: gray; color: black;"> CINZA'
        , '<span style="background-color: orange; color: black;"> LARANJA'
        , '<span style="background-color: navy blue; color: white;"> AQ MAR'];
    
    let splitter=[
      [0,0],
      ["A1 SEC.1 / A2 SEC.2 / A3 SEC.3 / A4 SEC.4 / A5 SEC.5 / A6 SEC.6 / A7 SEC.7 / A8 SEC.8"],
      ["A1 SEC.9 / A2 SEC.10 / A3 SEC.11 / A4 SEC.12 / A5 SEC.13 / A6 SEC.14 / A7 SEC.15 / A8 SEC.16"],
      ["A1 SEC.17 / A2 SEC.18 / A3 SEC.19 / A4 SEC.20 / A5 SEC.21 / A6 SEC.22 / A7 SEC.23 / A8 SEC.24"],
      ["A1 SEC.25 / A2 SEC.26 / A3 SEC.27 / A4 SEC.28 / A5 SEC.29 / A6 SEC.30 / A7 SEC.31 / A8 SEC.32"],
      ["A1 SEC.33 / A2 SEC.34 / A3 SEC.35 / A4 SEC.36 / A5 SEC.37 / A6 SEC.38 / A7 SEC.39 / A8 SEC.40"],
      ["A1 SEC.41 / A2 SEC.42 / A3 SEC.43 / A4 SEC.44 / A5 SEC.45 / A6 SEC.46 / A7 SEC.47 / A8 SEC.48"],
      ["A1 SEC.49 / A2 SEC.50 / A3 SEC.51 / A4 SEC.52 / A5 SEC.53 / A6 SEC.54 / A7 SEC.55 / A8 SEC.56"],
      ["A1 SEC.57 / A2 SEC.58 / A3 SEC.59 / A4 SEC.60 / A5 SEC.61 / A6 SEC.62 / A7 SEC.63 / A8 SEC.64"],
      ];
    
    var ss = prompt("Agora escreva na ordem os splitters secundários que contem na caixa \n exemplo: 5,4,3,7,4,3");
    
    var sss = ss.split(",");
     var x = "";
      
    for(var i = 0; i < sss.length; i++){
      var n = sss[i];
      var j = +n ;
    x = x + cores[i] + " SS"+ j + " >> " + splitter[n] + "<br/></span>";
    }
    
    document.getElementById("dgoi-c").innerHTML=x;

         }

        
         function sair(){
             window.close();
             alert("Obrigado, por utilizar o suporte avançado");
         }
        
       </script>
  
 </body>
</html>
