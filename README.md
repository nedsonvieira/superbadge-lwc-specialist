🚤 Superbadge Lightning Web Components Specialist – Friend Ships (HowWeRoll Rentals)
Este repositório contém a implementação da Superbadge Lightning Web Components Specialist do Trailhead, simulando o projeto Friend Ships para a HowWeRoll Rentals — a expansão para boat sharing usando ⚡ Lightning Web Components e 🧠 Apex.

🔗 Superbadge no Trailhead: Superbadge LWC Specialist
🔗 Repositório GitHub: github.com/nedsonvieira/superbadge-lwc-specialist

🎯 Descrição Geral
A aplicação simula o módulo Friend Ships, que expande a HowWeRoll Rentals para o compartilhamento de barcos. O objetivo principal:

⚓️ Visualização e edição de barcos
🗺️ Localização via mapa e geolocalização
✍️ Avaliações com sistema de estrelas
🧩 Boas práticas com LWC: componentização, pub/sub, navegação, feedback visual
🚀 Integração com Apex para dados e lógica de negócio

⚙️ Componentes Lightning Web Components
🧱 Abaixo, um resumo dos principais componentes:

🔍 boatSearch
Container principal da busca de barcos

Combina boatSearchForm + boatSearchResults

Exibe spinner (<lightning-spinner>) e botão “New Boat”

📋 boatSearchForm
Combobox para filtro por tipo de barco (via Apex)

Dispara evento search com boatTypeId

📦 boatSearchResults
Tabs: 🖼️ Gallery, ✏️ Boat Editor, 📍 Boats Near Me

Usa Lightning Message Service para comunicação

Toasts para feedback de sucesso/erro

🧩 boatTile
Card visual com informações básicas do barco

Alterna visual com CSS ao ser selecionado

Dispara evento boatselect

📍 boatsNearMe
Usa navigator.geolocation para localizar o usuário

Chama Apex para buscar barcos próximos

Mostra <lightning-map> com marcador “You Are Here”

🗺️ boatMap
Recebe boatId via Message Channel

Mostra a posição do barco em um mapa

Usa getRecord + spinner durante carregamento

⭐ fiveStarRating
Avaliação interativa com 5 estrelas

Editável ou somente leitura

Usa loadScript e loadStyle com recurso externo

🧾 boatDetailTabs
Tabs: 📄 Details, 📝 Reviews, ➕ Add Review

Usa NavigationMixin para links e botões

Chama refresh() após criação de review

🧑‍⚖️ boatAddReviewForm
Formulário editável com Subject, Comment e Rating

Dispara evento createreview ao salvar

Toasts de sucesso e limpa formulário

🧠 boatReviews
Lista de reviews com avatar, autor, data e comentário

Usa Apex imperativo e SLDS Feed Layout

Mensagem amigável se não houver avaliações

🤝 similarBoats
Exibe barcos similares (por tipo, preço ou tamanho)

Configurável via Lightning App Builder

Usa boatTile para mostrar resultados

✅ Requisitos
🛠️ Salesforce CLI

☁️ Org de desenvolvimento Salesforce

🧑‍💻 VS Code com Salesforce Extensions

📚 Recursos
📘 Documentação LWC
🎓 Trailhead: Superbadge LWC Specialist

👨‍💻 Autor
Nedson Vieira
🔗 LinkedIn
🌟 Trailhead Profile