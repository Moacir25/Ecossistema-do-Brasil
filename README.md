# Ecossistema-do-Brasil
var tela = 1, largura =150, altura = 30, xmenu = 135, ymenu1 = 180,ymenu2 = 245, ymenu3=310, ymenuvoltar = 360, Moacir, fundo, creditos, descricao,jogo,jogo01, eco1, correto, errado, cerrado, mata, mangue, cocais, pampas, arau, amaz, final;
// https://youtu.be/AGgchwjFxjw 

function preload(){
  //carregar imagem 
 
  fundo = loadImage('ecobrasil.png')
  creditos = loadImage('créditos.png')
  descricao = loadImage('descri.png')
  jogo = loadImage('jogo.png')
  Jogo01 = loadImage('Jogo01.png')
  eco01 = loadImage('eco01.png')
  correto = loadImage('correto.png')
  errado = loadImage('Errado.png')
  cerrado = loadImage('cerrado.png')
  mata = loadImage('mata.png')
  mangue = loadImage('mangue1.png')
  cocais = loadImage('cocais02.png')
  pampas = loadImage('pam.png')
  pantanal = loadImage('pantanal1.png')
  arau = loadImage('arau.png')
  amaz = loadImage('amaz1.png')
  final = loadImage('final.png')
  son = loadSound('erradoson.wav')
  win = loadSound('soncerto.wav')
  inicson = loadSound('sonIni.wav')
  parason = loadSound('parason.wav')
  menuson = loadSound('meson.wav')
  click = loadSound('sonclick.wav')
  







}
function setup() {
  createCanvas(400, 400);
}

function draw() {
   if(tela==1){
     //a tela 1 cpmeça aqui
    background(fundo);
    
    // botões
    if (mouseX<=xmenu+largura && mouseX>=xmenu && mouseY<=ymenu1+altura&& mouseY>=ymenu1){
      if (mouseIsPressed){
        inicson.play()
        tela=2
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    rect(xmenu,ymenu1,largura,altura,10)
    fill('black')
     textSize(15)
    textStyle(NORMAL)
    text('Jogar', xmenu+50,ymenu1+20)
    // segundo botão
    if (mouseX<=xmenu+largura && mouseX>=xmenu && mouseY<=ymenu2+altura&& mouseY>=ymenu2){
      if (mouseIsPressed){
         click.play()
        tela =4
        fill('red')
      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    rect(xmenu,ymenu2,largura,altura,10)
    fill('black')
    textStyle(NORMAL)
    text('Descrição', xmenu+45,ymenu1+85)
    // terceiro do botão

    if (mouseX<=xmenu+largura && mouseX>=xmenu && mouseY<=ymenu3+altura&& mouseY>=ymenu3){
      if (mouseIsPressed){
        click.play()
        tela=3
        fill('red')
         }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    rect(xmenu,ymenu3,largura,altura,10)
    fill('black')
    textStyle(NORMAL)
    text('Créditos', xmenu+50,ymenu1+150)
  // a tela 1 acaba aqui
   }
  
// tela 3 créditos do jogo começa aqui
  if(tela ==3){
    background(creditos)
   
    // botão voltar
    if (mouseX<=xmenu+largura && mouseX>=xmenu && mouseY<=ymenuvoltar+altura&& mouseY>=ymenuvoltar){
      if (mouseIsPressed){
        click.play()
        tela=1
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    rect(xmenu,ymenuvoltar,largura,altura,10)
    fill('black')
    textStyle(NORMAL)
    text('Voltar', xmenu+50,ymenuvoltar+23)
   
   
  }
  //tela de descrição 
  if(tela==4){
    background(descricao)
    //botão voltar descrição
    ymenu4= 360
    if (mouseX<=xmenu+largura && mouseX>=xmenu && mouseY<=ymenu4+altura&& mouseY>=ymenu4   )       {
      if (mouseIsPressed){
        click.play()
        tela=1
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    rect(xmenu,ymenu4,largura,altura,10)
    fill('black')
    textStyle(NORMAL)
    text('Voltar', xmenu+50,ymenu4+23)
    
    
    
    
  }
  if(tela==2){
    background(jogo)
    //tela jogo
    ymenu5= 282
    if (mouseX<=xmenu+largura && mouseX>=xmenu && mouseY<=ymenu5+altura&& mouseY>=ymenu5   )       {
      if (mouseIsPressed){
        tela=5
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    rect(xmenu,ymenu5,largura,altura,10)
    fill('black')
    textStyle(NORMAL)
    text('Iniciar', xmenu+50,ymenu5+20)
    
    
    
    
  }
  if(tela==5){
     //a primeira tela do jogo comaça aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 1',130,25)
    image(eco01,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da primeira tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
        menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
        son.play()
        tela = 5.2
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Amazônia', xjogo1+20,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
        win.play()
        tela = 5.1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Caatinga', xjogo1+20,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 5.2
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Cerrado', xjogo1+25,yjogo2+15)
    // a primeira tela do jogo acaba aqui
    
   }
  if(tela==5.1){
     //tela de resposta correta
    background(correto)
    
   
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões voltar
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 6
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
    
   
   
   }
    // tela de resposta errada
  if(tela==5.2){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 5
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==6){
     //a segunda tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 2',130,25)
    image(cerrado,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da segunda tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
        son.play()
        tela = 5.4
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata atlântica', xjogo1+9,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
        son.play()
        tela = 5.4
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Pampas', xjogo1+20,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
         win.play()
        tela = 5.3
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Cerrado', xjogo1+25,yjogo2+15)
    // a segunda tela do jogo acaba aqui
    
   }
  if(tela==5.3){
     //tela de resposta correta
    background(correto)
    
   
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões voltar
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
        menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 7
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
    
   
   
   }
  //tela de resposta errada
  if(tela==5.4){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 6
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==7){
     //a terceira tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 3',130,25)
    image(mata,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da terceira tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
         win.play()
        tela = 5.5
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata atlântica', xjogo1+9,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
        son.play()
        tela = 5.6
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mangue', xjogo1+20,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 5.6
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata Cocais', xjogo1+15,yjogo2+15)
    // a terceira tela do jogo acaba aqui
    
   }
  if(tela==5.5){
     //tela de resposta correta
    background(correto)
    
   
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões voltar
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 8
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
    
   
   
   }
  //tela de resposta errada
  if(tela==5.6){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 7
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==8){
     //a quarta tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 4',130,25)
    image(mangue,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da quarta tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
        son.play()
        tela = 5.8
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Amazônia', xjogo1+9,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
         win.play()
        tela = 5.7
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mangue', xjogo1+20,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 5.8
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata Cocais', xjogo1+15,yjogo2+15)
    // a quarta tela do jogo acaba aqui
    
   }
  if(tela==5.7){
     //tela de resposta correta
    background(correto)
   
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 9
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
   
   }
  //tela de resposta errada
  if(tela==5.8){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 8
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==9){
     //a quinta tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 5',130,25)
    image(cocais,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da quinta tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
        son.play()
        tela = 5.01
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Pantanal', xjogo1+15,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
         win.play()
        tela = 5.9
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata Cocais', xjogo1+15,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 5.01
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Pampas', xjogo1+20,yjogo2+15)
    // a quinta tela do jogo acaba aqui
    
   }
  if(tela==5.9){
     //tela de resposta correta
    background(correto)
   
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 10
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
   
   }
  //tela de resposta errada
  if(tela==5.01){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 9
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==10){
     //a sexta tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 6',130,25)
    image(pampas,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da sexta tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
         win.play()
        tela = 7.1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Pampas', xjogo1+20,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
        son.play()
        tela = 7.2
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata Araucária', xjogo1+5,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 7.2
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Savana', xjogo1+23,yjogo2+15)
    // a sexta tela do jogo acaba aqui
    
   }
  if(tela==7.1){
     //tela de resposta correta
    background(correto)
   
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 11
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
   
   }
  //tela de resposta errada
  if(tela==7.2){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 10
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==11){
     //a sétima tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 7',130,25)
    image(pantanal,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da sétima tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
         win.play()
        tela = 20
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Pantanal', xjogo1+20,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
        son.play()
        tela = 21
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Cocais', xjogo1+25,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 21
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Amazônia', xjogo1+23,yjogo2+15)
    // a sétima tela do jogo acaba aqui
    
   }
  if(tela==20){
     //tela de resposta correta
    background(correto)
   
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 12
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
   
   }
  //tela de resposta errada
  if(tela==21){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 11
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==12){
     //a oitava tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 8',130,25)
    image(arau,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da oitava tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
        son.play()
        tela = 31
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Amazônia', xjogo1+20,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
        son.play()
        tela = 31
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Cocais', xjogo1+25,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
         win.play()
        tela = 30
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata Araucária', xjogo1+4,yjogo2+15)
    // a oitava tela do jogo acaba aqui
    
   }
  if(tela==30){
     //tela de resposta correta
    background(correto)
   
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 13
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Continuar', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
   
   }
  //tela de resposta errada
  if(tela==31){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 12
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  if(tela==13){
     //a nona tela do jogo começa aqui
    background(Jogo01)
    
    
    
    fill('black')
     textSize(25)
    textStyle(BOLD)
    text('Nível 9',130,25)
    image(amaz,230,150,150,150)
    xjogo = 230
    larguraj = 80
    yjogo = 10
    altura02 = 20
    // botões da nona tela do jogo
    
    if (mouseX<=xjogo+larguraj && mouseX>=xjogo && mouseY<=yjogo+altura&& mouseY>=yjogo){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo,yjogo,larguraj,altura02,10)
    fill('white')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xjogo+23,yjogo+15)
    
   xjogo1 = 50
    largurajo = 100
    yjogo0 = 200
    yjogo1 = 235
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo0+altura02&& mouseY>=yjogo0){
      if (mouseIsPressed){
        son.play()
        tela = 41
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo0,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Mata Atlântica', xjogo1+8,yjogo0+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo1+altura02&& mouseY>=yjogo1){
      if (mouseIsPressed){
         win.play()
        tela = 40
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo1,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Amazônia', xjogo1+20,yjogo1+15)
    
    if (mouseX<=xjogo1+largurajo && mouseX>=xjogo1 && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        son.play()
        tela = 41
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('green')

    }
    
    rect(xjogo1,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Pantano', xjogo1+25,yjogo2+15)
    // a nona tela do jogo acaba aqui
    
   }
  if(tela==40){
     //tela de resposta correta
    background(correto)
   
    //botão continuar
   xcorreto = 290
    largurajo = 100
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xcorreto+largurajo && mouseX>=xcorreto && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        parason.play()
        tela = 14
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xcorreto,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Concluir', xcorreto+20,yjogo2+15)
     // a tela de resposta correta acaba aqui
   
   }
  //tela de resposta errada
  if(tela==41){
    background(errado)
    
    //botão tentar novamente 
   xerrado = 265
    largurajo = 130
    yjogo2 = 270
    altura02 = 20
    
    if (mouseX<=xerrado+largurajo && mouseX>=xerrado && mouseY<=yjogo2+altura02&& mouseY>=yjogo2){
      if (mouseIsPressed){
        tela = 13
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrado,yjogo2,largurajo,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Tente novamente', xerrado+11,yjogo2+15)
     // a tela de resposta errada acaba aqui
    
   
   
   }
  //conclusão 
  if(tela==14){
    background(final)
    
    //botão menu
   xerrad = 135
    largurajog = 130
    yjogo21 = 290
    altura021 = 20
    
    if (mouseX<=xerrad+largurajog && mouseX>=xerrad && mouseY<=yjogo21+altura02&& mouseY>=yjogo21){
      if (mouseIsPressed){
         menuson.play()
        tela = 1
        
        
        fill('red')

      }else{
        fill('blue')
      }

    }else{
      fill('white')

    }
    
    rect(xerrad,yjogo21,largurajog,altura02,10)
    fill('black')
     textSize(14)
    textStyle(NORMAL)
    text('Menu', xerrad+45,yjogo21+15)
     // a tela de conclusão
    
   
   
   }
  
  
  
  
}
