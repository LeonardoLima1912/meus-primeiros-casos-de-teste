# BUG-01 - Botão "Cadastrar" não responde no navegador Safari

**Severidade:** Alta  
**Prioridade:** Alta  
**Ambiente:** macOS Sonoma 14.2 / Safari v17.1  

---

### **Descrição**
Ao preencher todos os campos obrigatórios no formulário de cadastro e clicar no botão "Cadastrar", a página não executa nenhuma ação nem exibe mensagens de validação ou sucesso.

---

### **Passos para Reproduzir**
1. Acessar a página `https://exemplo.com/cadastro` via navegador Safari.
2. Preencher os campos com dados válidos:
   - **Nome:** Leonardo
   - **E-mail:** leonardo.novo@teste.com
   - **Senha:** Senha@123
3. Clicar no botão **"Cadastrar"**.

---

### **Resultado Esperado**
O usuário deve ser redirecionado para a página de boas-vindas (`/dashboard`) com a sessão iniciada.

### **Resultado Obtido**
O botão permanece clicável, porém nenhuma requisição é enviada e a tela permanece estática sem qualquer feedback visual.

---

### **Evidências & Anexos**
- *Console do navegador (DevTools):* `Uncaught TypeError: Cannot read properties of undefined (reading 'submit')`
- 
