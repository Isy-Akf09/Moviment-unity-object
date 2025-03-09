# Como fazer um objeto de mover na Unity engine.
 - Como criar um codigo para movimentar um objeto na Unity engine


# Introdução
- Criando um objeto 3D:

Com o projeto criado e abento no Unity, você pode adcionar um novo objeto 3D para a cena;
isso pode ser feito na aba hierarquia, botão superior esquerdo:
<div>
 <img src="https://github.com/user-attachments/assets/bc9e1bf0-f1ef-4005-a8e2-3636dca28eee" width=500px />
</div>
Crie o Objeto 3D de sua preferencia:

![Image](https://github.com/user-attachments/assets/df30a37d-f616-45c5-a1a8-e8a03eafd335)

No caso demonstrado, iremos utilizar um simples cubo.

# Criando o Script
- Criando a pasta Script:

Com o objeto feito, vá para a aba project, e em Assets, Clique com o botão Direito
em cima da pasta e vá em create -> folder:

![Image](https://github.com/user-attachments/assets/6b83e2bf-c20f-4e06-ac06-0714fe19ed9d)
![Image](https://github.com/user-attachments/assets/a1cb5f9c-656a-4598-bd76-6c711c011d83)

Nome-e a Pasta como "Scripts", e com botão direito em cima dela, Vai em create -> "C# Script";
Isso criará um arquivo para o codigo que iremos utilizar para movimentar o Objeto:

![Image](https://github.com/user-attachments/assets/ded8f036-2fd6-4a89-a889-f9533b3bb7a4)
![Image](https://github.com/user-attachments/assets/da0e6162-cb2a-4c5a-be88-c69ed0a56c33)

Após criar o arquivo nomeie ele como "MoveNomedoobjeto", se voce clicar duas vezes,
ele abrirá automaticamente o deu IDE para começar a programar o codigo:

![Image](https://github.com/user-attachments/assets/3eae8cc6-ddbc-4262-bf5a-9adb984dfac1)

O Codigo automatico da Unity provavelmente estará assim:

![Image](https://github.com/user-attachments/assets/c237064b-87ac-46e4-bee9-67ee716afc3c)

- Criando o Codigo:
  
No seu IDE, Exclue apartir do "Void Start()", e aplique o seguinte codigo:

      using UnityEngine;
      
      public class MoveCube : MonoBehaviour
      {
          //Definir a velocidade do movimento do objeto.
          public float speed = 10f;
      
          void Update() //Atualiza de acordo com os FPS.
          {
              //Criando variavel do eixo HORIZONTAL.
              float moveHorizontal = Input.GetAxis("Horizontal");
              //Criando variavel do eixo VERTICAL.
              float moveVertical = Input.GetAxis("Vertical");
      
             //Criando a variavel vetor pro movimento com 3 espaços.
             Vector3 movement = new Vector3(moveHorizontal, 0, moveVertical);
     
              transform.Translate(movement * speed * Time.deltaTime);
          }
      }

Após isso, voce deve salvar o arquivo usando "Ctrl + S" (Windows), ou "Cmd + S" (Mac);

- Vinculando o Script no objeto:

Voltando na Unity, ela deve recopilar o codigo automaticamente, caso não tenha feito isso,
verifique se você salvou corretamente em seu IDE;
No Inspetor, com o arquivo do Script selecionado é possivel ver o nosso codigo:

![Image](https://github.com/user-attachments/assets/2fae286f-4429-4fb9-9b3a-2a96fdaa8715)

Verifique se o codigo está completo e correto de acordo com o que você fez.
Após verificar se tudo está corretamente aplicado, Selecione o Objeto em sua 
cena ou na aba hierarquia:

![Image](https://github.com/user-attachments/assets/78f30adf-8c97-4ef5-8723-f404335fa655)

Na aba do Inspetor, vai em "Add Component"
![Image](https://github.com/user-attachments/assets/e7b38fb3-8d06-493d-9cce-343c8728cbb1)

Pesquise pelo nome do arquivo script e selecione, isso irá vincular o Objeto
com o script:

![Image](https://github.com/user-attachments/assets/a8897e35-21b4-4891-b88f-725289ae7acb)

Pronto! O Objeto está vinculado com sucesso no codigo script!

# Testes
- Testando o Script:

Clique no "Play" No centro superior da tela e isso irá iniciar a simulação do Jogo,
Faça quantos testes você precisar para para produzir o seu Jogo com total sucesso! :D

https://github.com/user-attachments/assets/03a1fef0-160a-485b-bbe8-5115604fb580

Deus abençõe Vocês! ^^
