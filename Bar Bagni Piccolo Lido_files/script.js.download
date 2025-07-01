fetch('menu.json')
  .then(res => res.json())
  .then(data => {
    const menuContainer = document.getElementById('menu');

    data.forEach(categoria => {
      const titolo = document.createElement('h2');
      titolo.textContent = categoria.categoria;
      menuContainer.appendChild(titolo);

      categoria.elementi.forEach(item => {
        const div = document.createElement('div');
        div.className = 'menu-item';

        div.innerHTML = `
          <img src="${item.immagine}" alt="${item.nome}" />
          <h3>${item.nome}</h3>
          <p><strong>Banco:</strong> ${item.prezzo_banco}</p>
          <p><strong>Tavolo:</strong> ${item.prezzo_tavolo}</p>
        `;
        menuContainer.appendChild(div);
      });
    });
  })
  .catch(error => {
    document.getElementById('menu').innerHTML = "Errore nel caricamento del menù.";
    console.error('Errore:', error);
  });