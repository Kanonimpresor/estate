# Estate
Plugin para Gestão de Agências Imobiliárias no e107

## Descrição
Um plugin para o Sistema de Gestão de Conteúdo e107 que permite gerir Agências Imobiliárias, Agentes e Listagens. Este plugin começou como uma forma de um Agente Imobiliário individual listar facilmente as suas propriedades para venda e evoluiu para um sistema que pode lidar com múltiplos agentes e agências.

## Demonstração
Pode ver um site em produção utilizando este plugin em:
https://www.sandpiperhome.org

## Atualização Manual Durante o Desenvolvimento
1. Para atualizar no seu website durante o desenvolvimento:
2. Faça download de TODOS os ficheiros
3. Substitua todos os ficheiros existentes no seu website pelos atuais

Pode encontrar os ficheiros mais recentes aqui:
https://github.com/Vodhin/estate/releases

# Instruções para Substituição de Ficheiros

Por favor, substitua todos os **ficheiros**, da versão anterior, nas seguintes localizações:

1. `estate/css` - Substitua todos os ficheiros
2. `estate/js/adm` - Substitua todos os ficheiros
3. `estate/js` - Apenas ficheiros (não substitua outras pastas)
4. `estate/languages/English` - Substitua todos os ficheiros
5. `estate/templates` - Substitua todos os ficheiros
6. `estate/ui` - Substitua todos os ficheiros
7. `estate/xml` - Substitua todos os ficheiros (exclua a pasta 'sample' se existir)
8. `estate/` - Todos os ficheiros principais (não substitua `.gitattributes` ou `README.md`)

Notas importantes:
- Mantenha a estrutura original de pastas
- Não elimine quaisquer pastas, apenas substitua os ficheiros
- Os ficheiros de configuração (como `.gitattributes`) devem ser preservados
- A pasta 'sample' no diretório XML não deve ser alterada

# Verificações de Base de Dados do e107
## Operações de Manutenção
  * Verificar e Guardar Preferências na secção de Administração do Estate
  * Limpar Cache e verificar páginas

# Histórico de Desenvolvimento/Revisões

## 📅 29 Dezembro 2024
- **Correção de bugs** em funcionalidades específicas
- **Novos dados predefinidos** para:
  - Propriedades
  - Comunidades/Empreendimentos
  - Características de Cidades
- **Shortcodes** adicionados para exibição de informações

## 📅 27 Novembro 2024
- **Sistema de formatação** renovado:
  - Moedas baseadas em PHP Locale
  - Formatação de datas regionalizada
- **Novo formulário financeiro** que substitui os campos antigos (mantidos ocultos)
  - Tabela de histórico de preços
  - Modelos personalizáveis de listagem (editáveis na Admin ou diretamente na página)

## 📅 4 Outubro 2024
- **Correções múltiplas**
- **Novos campos**:
  - Descrição para informações de cidade
  - Funcionalidade "Espaços Urbanos"
- Verificação automática de pastas de media
- Correção de configurações padrão (agradecimentos a jimmi08)
- **Planeado**: Seleção de moeda baseada no país da propriedade

## ⚠️ 15 Setembro 2024
- **Ação manual necessária**:
  - Remover `space_propidx` via phpMyAdmin
  - Executar atualização da base de dados
- Alterações na estrutura da BD e preferências

## 📅 7 Setembro 2024
- **Atualização obrigatória** da base de dados
- Nova função "Desfazer" para formulários de Empreendimentos

## 📅 25 Agosto 2024
- **Melhorias significativas**:
  - Sistema de informação comunitária
  - Partilha de dados entre propriedades vizinhas
- Correções menores de bugs

## 📅 7 Julho 2024
- **Sistema de moderação** para listagens de particulares:
  - Aprovação automática ou manual
  - Notificações por email para moderadores
  - Seleção de moderadores entre:
    - Gestores Imobiliários
    - Admins Imobiliários
    - Admins do Site

## 📅 27 Junho 2024
- **Novo painel** (e_dashboard)
- Campos adicionais na BD
- Requer após atualização:
  - Atualização da BD
  - Verificação de diretórios

## 📅 26 Junho 2024
- **Compatibilidade** com PHP 8.2.2
- Diversos refinamentos

## 📅 16 Junho 2024
- **Sistema de contacto integrado**:
  - 4 tipos de comunicação pré-definidos
  - Notificações por email e MP
  - Proteção anti-spam com:
    - Campos ocultos
    - Verificação JavaScript

## 📅 5 Maio 2024
- Preparação para versão estável
- **Funcionalidades em desenvolvimento**:
  - Formulários de informação comunitária
  - Elementos UI para:
    - Favoritos
    - Histórico de comunicações

# REQUISITOS DO SISTEMA
## Versão do e107
Versão mínima necessária: e107 v2.3.3 ou superior

Compatibilidade com PHP
Versões testadas e suportadas:
✅ PHP 7.4.33 (estável)

Versões mais recentes de PHP:
⚠️ Podem causar problemas (em resolução)

## Notas Adicionais:
  * Este plugin está em desenvolvimento ativo, com melhorias contínuas na compatibilidade com versões mais recentes do PHP.
  * Recomenda-se verificar atualizações regularmente para garantir o funcionamento ideal.
  * Problemas conhecidos com PHP 8.x estão a ser corrigidos em atualizações futuras.

# CARACTERÍSTICAS PRINCIPAIS

## 👥 Gestão de Utilizadores
- **Atribuição de funções**:
  - Agentes Imobiliários
  - Gestores de Agência
  - Administradores de Agência
- **Validação de utilizadores** que previne acessos não autorizados a outras áreas de administração fora deste plugin
- **Formulário rápido de adição de utilizador** integrado para criar novos perfis de Utilizador e Agente diretamente no plugin Estate

## 🏡 Perfis Personalizados
- **Perfis de Agente** vinculados a Perfis de Utilizador
- **Base de dados multi-tabela** para armazenar informação comum partilhada entre listagens de propriedades

## 🛠 Ferramentas Avançadas
- **Menus dropdown editáveis** diretamente nos formulários
- **Opções de dados partilhados** entre listagens
- **Integração com Leaflet Maps** para visualização de:
  - Listagens de propriedades
  - Localizações de agências

## 🖼 Gestão de Imagens
- **Carregamento múltiplo de imagens** via AJAX
- **Galerias separadas**:
  - Baseadas em divisões/áreas
  - Galeria geral da propriedade
- **Reordenamento de imagens** por arrastar e soltar
- **Recorte de imagens no navegador** com integração CropperJS ([fengyuanchen.github.io/cropperjs/](https://fengyuanchen.github.io/cropperjs/))

## 💡 Sistema de Ajuda
- **Barra lateral dinâmica** e ajuda contextual adaptada a:
  - Nível de acesso do utilizador
  - Predefinições ativadas
- **Ajuda abrangente** com informações relevantes para:
  - Formulário atual
  - Separadores selecionados

## 🎨 Personalização
- **Templates front-end** personalizáveis através do formulário de Preferências do Estate
- **Funcionalidade rápida de adição/edição** no front-end
- **Listagens privadas para não-agentes** (Venda por Proprietário) disponível para classe de utilizador selecionada

## ✉️ Comunicação
- **Formulário de contacto** Agente/Vendedor com:
  - Notificações por email
  - Integração com sistema de Mensagens Privadas (PM)
