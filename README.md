# 🔍 Verificador de Notas SAP para o Ecossistema PIX

Utilitário em ABAP desenvolvido para consultar rapidamente o status de aplicação das notas de localização do ecossistema **PIX (Localização Brasil)** nos ambientes SAP (ECC / S/4HANA). 

O programa realiza uma varredura cruzando as principais notas requeridas pela SAP (como o framework de PIX e rotinas de criação de dados bancários) com o histórico de notas aplicadas no sistema via `SNOTE`, facilitando o diagnóstico de pendências em projetos de implementação ou rollouts.

---

## 🚀 Como Implementar no Ambiente

Siga o passo a passo abaixo para criar e executar o programa no seu ambiente SAP:

### 1. Criação do Programa
1. Acesse a transação **`SE38`** (ou `SE80`).
2. No campo **Programa**, informe o nome: `ZSAP_CHECK_NOTES_PIX` e clique em **Criar**.
<img width="923" height="638" alt="Criar programa na SE38" src="https://github.com/user-attachments/assets/4274dd92-8f04-44a6-b6fa-b73de50f73d2" />

### 2. Inserção do Código Fonte
3. Copie o código fonte contido no arquivo deste repositório e cole-o diretamente no editor ABAP.

### 3. Verificação, Salvamento e Ativação
4. Clique no botão de **Verificar** (ou pressione `Ctrl + F2`) para validar a sintaxe do código.
<img width="943" height="332" alt="Verificar código" src="https://github.com/user-attachments/assets/241d71b7-ae79-47af-b087-6bcfdff38162" />

5. Salve o programa (`Ctrl + S`) vinculado ao pacote de desenvolvimento local (`$TMP`) ou de sua preferência.
6. Ative o programa clicando no botão de **Ativar** (ou pressione `Ctrl + F3`).
<img width="514" height="562" alt="Ativar programa" src="https://github.com/user-attachments/assets/2c90020e-6bfb-4475-bf66-8996e831eac9" />

---

## 📊 Como Utilizar e Visualizar as Notas Faltantes

1. Com o programa ativo, retorne à tela inicial da `SE38` (ou utilize a transação `SA38`), informe `ZSAP_CHECK_NOTES_PIX` e clique em **Executar** (`F8`).
<img width="433" height="261" alt="Tela de execução" src="https://github.com/user-attachments/assets/d559a085-13ea-41aa-9dee-6bfd46c3f4eb" />

<img width="376" height="238" alt="Executar relatório" src="https://github.com/user-attachments/assets/3cbf513d-4211-4126-809e-c601ce465559" />

2. O relatório exibirá de forma estruturada o status de cada nota do PIX, permitindo identificar de maneira ágil quais correções ainda precisam ser aplicadas via `SNOTE`.
<img width="1919" height="1088" alt="Resultado da execução" src="https://github.com/user-attachments/assets/c82a428a-9c6e-4818-8d56-298042f2c165" />
