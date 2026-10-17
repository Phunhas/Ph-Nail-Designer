# PH Nail Designer

Site de agendamento da PH Nail Designer. A cliente escolhe os serviços, escolhe o horário e finaliza pelo WhatsApp com a mensagem já pronta.

## Arquivos

| Arquivo | Para que serve |
|---|---|
| `index.html` | O site que as clientes veem |
| `config.json` | Valores, horários, contatos e aviso (é o que o painel edita) |
| `og.png` | Imagem que aparece quando o link é enviado no WhatsApp/Instagram |
| `admin.html` | Painel para mudar valores e horários pelo celular |
| `logo.png` | Opcional. Se existir, aparece no topo no lugar do "PH" em texto |

## Colocar no ar (GitHub Pages)

1. No repositório, vá em **Settings → Pages**.
2. Em **Build and deployment**, escolha **Deploy from a branch**.
3. Em **Branch**, escolha `main` e a pasta `/ (root)`, e clique em **Save**.
4. Espere cerca de 1 minuto. O endereço aparece na mesma tela: `https://usuario.github.io/nome-do-repositorio/`.

O GitHub Pages grátis exige repositório **público**.

## Mudar valores e horários pelo painel

Abra `https://usuario.github.io/nome-do-repositorio/admin.html`.

Na primeira vez em cada aparelho, o painel pede um **token** do GitHub:

1. No GitHub: foto do perfil → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Dê um nome (ex.: `painel-ph`) e escolha uma validade.
3. Em **Repository access**, escolha **Only select repositories** e marque só este repositório.
4. Em **Permissions → Repository permissions**, coloque **Contents: Read and write**.
5. Gere e copie o token. Ele só aparece uma vez.
6. Cole o token no painel, junto com o nome do repositório (`usuario/nome-do-repositorio`), e toque em **Conectar e carregar**.

No painel dá para:
- mudar nome, preço e observação de cada serviço, adicionar, remover e reordenar;
- adicionar e remover horários;
- marcar horários como **ocupados em um dia específico** (card "Agenda por dia"): escolha a data e toque nos horários reservados, ou marque o dia todo. Só aquele dia muda; dias passados saem sozinhos. As clientes escolhem entre os próximos 7 dias;
- enviar **fotos dos trabalhos**: escolha as fotos no celular e toque em "Enviar fotos para o site". Elas são reduzidas sozinhas e aparecem na seção "Meus Trabalhos". Dá para escrever uma legenda (salva em "Salvar no site") e remover fotos. Se não houver nenhuma foto, a seção não aparece no site;
- editar as **perguntas frequentes** e o **endereço** (com botão "Como chegar"); se estiverem vazios, a seção não aparece;
- ligar o **contador de visitas** (GoatCounter, grátis): crie a conta em goatcounter.com, escolha um código e digite o mesmo código no painel;
- escrever um **aviso** que aparece no topo do site;
- mudar WhatsApp, Instagram e e-mail.

Depois de **Salvar no site**, a mudança aparece em cerca de 1 minuto.

### Cuidados com o token

- Ele fica salvo só no aparelho onde foi digitado. Não compartilhe com ninguém.
- Quem tem o token consegue alterar os arquivos deste repositório. Por isso, crie o token só para este repositório.
- Se perder o celular ou suspeitar de vazamento, apague o token em **Settings → Developer settings** no GitHub.
- O endereço `/admin.html` é público, mas sem o token ninguém consegue salvar nada.

## Logo

Para usar a logo real, salve a imagem como `logo.png` (fundo transparente funciona melhor) na pasta do site. Nada mais precisa mudar.

## Editar à mão

Se preferir, edite o `config.json` direto no GitHub (ícone de lápis). Os preços são números (`50` ou `42.5`) e os horários ficam no formato `"09:00"`.
