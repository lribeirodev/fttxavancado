<html>
<head>
 <title>
   Suporte Avançado
 </title>
</head>

 <body>
   
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
    
    var cores = ['VERDE' ,'AMARELO', 'BRANCO', 'AZUL', 'VERMELHO', 'VIOLETA', 'MARROM', 'ROSA', 'PRETO', 'CINZA', 'LARANJA', 'AQ MAR'];
    
    let splitter=[
      [0,0],
      [1,2,3,4,5,6,7,8],
      [9,10,11,12,13,14,15,16],
      [17,18,19,20,21,22,23,24],
      [25,26,27,28,29,30,31,32],
      [33,34,35,36,37,38,39,40],
      [41,42,43,44,45,46,47,48],
      [49,50,51,52,53,54,55,56],
      [57,58,59,60,61,62,63,64]
      ];
    
    var ss = prompt("Agora escreva na ordem os splitters secundários que contem na caixa \n exemplo: 5,4,3,7,4,3");
    
    var sss = ss.split(",");
     var x = "";
      
    for(var i = 0; i < sss.length; i++){
      var n = sss[i];
      var j = +n ;
    x = x + cores[i] + " SS"+ j + " " + splitter[n] + "\n";
    }
    
    alert(x);
         menu();
         }

        
         function sair(){
             window.close();
             alert("Obrigado, por utilizar o suporte avançado");
         }
        
       </script>
  
 </body>
</html>
