# Memories - Diário Digital Full-Stack

## 📚 Propósito do Projeto
Este projeto foi desenvolvido de forma guiada durante uma formação, com o objetivo principal de aprendizado e fixação de conceitos práticos. A autoria da ideia e do design original pertencem ao curso. Este repositório serve para demonstrar minha capacidade de compreender, codificar, integrar e estender uma aplicação completa utilizando React, Node.js e MongoDB, com foco especial na manipulação e upload de arquivos.

## 💻 Sobre o Projeto
O **Memories** é uma aplicação interativa que funciona como um mural de lembranças digital. A plataforma permite que o usuário eternize momentos criando postagens que contêm título, descrição e o upload de uma fotografia. 

Além da criação, o sistema permite interações detalhadas com cada lembrança, como a funcionalidade de favoritar momentos especiais e a adição de comentários contínuos em cada postagem.

## 🛠️ Tecnologias Utilizadas

### **Frontend**
* **React (Vite):** Biblioteca principal para construção da interface.
* **React Router DOM:** Gerenciamento de rotas para navegação entre o mural e a visualização individual da lembrança.
* **Axios:** Cliente HTTP para comunicação com a API REST.
* **React Toastify:** Sistema de notificações para feedbacks de sucesso ou erro (ex: falha no upload).

### **Backend**
* **Node.js & Express:** Ambiente de execução e framework para o servidor.
* **MongoDB & Mongoose:** Banco de dados NoSQL e ODM para persistência das informações.
* **Multer:** Middleware crucial para lidar com dados `multipart/form-data`, responsável por processar e armazenar o upload das imagens.
* **CORS:** Configuração para permitir a comunicação com o frontend.

## 🚀 Funcionalidades e Conceitos Aplicados

* **Upload de Arquivos (Frontend e Backend):** Implementação de formulários utilizando o objeto `FormData` no React para enviar imagens. No backend, configuração do `multer` para interceptar a requisição, renomear o arquivo (evitando colisões) e salvá-lo no disco local (`/public/images`).
* **Arquitetura API RESTful Avançada:** Rotas estruturadas não apenas para o CRUD básico de lembranças, mas também rotas específicas para interações secundárias (adicionar comentários e alternar status de favorito).
* **Serviço de Arquivos Estáticos:** Configuração do Express (`express.static`) para expor a pasta de imagens, permitindo que o frontend consuma e renderize as fotos salvas através de URLs dinâmicas.
* **Atualizações Parciais (PATCH):** Uso de requisições do tipo PATCH para modificar partes específicas de um documento no MongoDB (como adicionar um comentário em um array ou inverter um booleano de favorito), otimizando a transferência de dados.
