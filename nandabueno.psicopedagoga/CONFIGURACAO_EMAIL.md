# Configuração do Sistema de Email - EmailJS

## Dados Atualizados ✓
- **WhatsApp:** https://wa.me/5551996475102
- **Email:** nandabuenopsicopedagoga@gmail.com
- **Formulário:** Configurado para enviar mensagens para seu email

## Como Configurar o EmailJS

### Passo 1: Registre-se no EmailJS
1. Acesse https://www.emailjs.com/
2. Clique em "Sign Up for Free" (ou faça login se já tem conta)
3. Confirme seu email

### Passo 2: Configure o Serviço de Email (Gmail)
1. No dashboard do EmailJS, clique em **Email Services**
2. Clique em **Add Service**
3. Selecione **Gmail**
4. Siga as instruções para conectar sua conta Gmail (nandabuenopsicopedagoga@gmail.com)
5. Salve o **Service ID** (vai parecer com: `service_xxxxx`)

### Passo 3: Crie um Email Template
1. Clique em **Email Templates**
2. Clique em **Create New Template**
3. Nomeie como: `contact_form`
4. Configure o template assim:

**TO_EMAIL:**
```
{{to_email}}
```

**SUBJECT:**
```
Nova mensagem de contato de {{from_name}}
```

**HTML_MESSAGE:**
```html
<p><strong>Nome:</strong> {{from_name}}</p>
<p><strong>Email:</strong> {{from_email}}</p>
<p><strong>WhatsApp:</strong> {{phone}}</p>
<p><strong>Mensagem:</strong></p>
<p>{{message}}</p>
```

5. Salve o template e copie o **Template ID** (vai parecer com: `template_xxxxx`)

### Passo 4: Obtenha a Public Key
1. No dashboard, clique em **Account**
2. Copie a **Public Key** (vai parecer com: `xxxxxxxxxxxxx`)

### Passo 5: Atualize o arquivo script.js
Abra o arquivo `script.js` e substitua:

- `COLOQUE_AQUI_SUA_PUBLIC_KEY_DO_EMAILJS` → Cole sua **Public Key**
- `COLOQUE_AQUI_SUA_SERVICE_ID_DO_EMAILJS` → Cole seu **Service ID**
- `COLOQUE_AQUI_SUA_TEMPLATE_ID_DO_EMAILJS` → Cole seu **Template ID**

### Exemplo:
```javascript
emailjs.init({
  publicKey: 'abc123def456xyz789'
});

emailjs.send(
  'service_7a8b9c0d1e2f3g4h',
  'template_9x8y7z6w5v4u3t2s',
  formData
);
```

## Testando
1. Abra seu site
2. Vá para a seção "Dê o primeiro passo" (Contato)
3. Preencha o formulário
4. Clique em "Enviar mensagem"
5. Você deve receber o email em nandabuenopsicopedagoga@gmail.com

## Suporte
- Documentação EmailJS: https://www.emailjs.com/docs/
- Tutorial em vídeo: https://www.youtube.com/watch?v=W6A4P0Rk5U4

---
**Nota:** O EmailJS tem um plano gratuito que permite enviar até 200 emails por mês. Isso é suficiente para um pequeno site de psicopedagoga. Se precisar de mais, há planos pagos muito acessíveis.
