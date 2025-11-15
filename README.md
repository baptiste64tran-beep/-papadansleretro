let panier = [];
let total = 0;

function ajouterPanier(produit, prix) {
    panier.push({ produit, prix });
    total += prix;
    afficherPanier();
}

function afficherPanier() {
    const liste = document.getElementById("liste-panier");
    liste.innerHTML = "";
    panier.forEach(item => {
        const li = document.createElement("li");
        li.textContent = `${item.produit} - ${item.prix} €`;
        liste.appendChild(li);
    });
    document.getElementById("total").textContent = total;
}
