let carrito = [];
let total = 0;

function agregarCarrito(nombre, precio) {
    carrito.push({nombre, precio});
    total += precio;
    actualizarCarrito();
    animacionAgregar();
}

function actualizarCarrito() {
    const lista = document.getElementById('lista-carrito');
    const totalSpan = document.getElementById('total');

    lista.innerHTML = '';

    carrito.forEach(producto => {
        const li = document.createElement('li');
        li.textContent = `${producto.nombre} - $${producto.precio.toLocaleString()}`;
        lista.appendChild(li);
    });

    totalSpan.textContent = total.toLocaleString();
}

// Vaciar carrito
document.getElementById('vaciar-carrito').addEventListener('click', () => {
    carrito = [];
    total = 0;
    actualizarCarrito();
});

// Abrir y cerrar carrito
const carritoDiv = document.getElementById('carrito');
document.getElementById('abrir-carrito').addEventListener('click', () => {
    carritoDiv.classList.add('visible');
});
document.getElementById('cerrar-carrito').addEventListener('click', () => {
    carritoDiv.classList.remove('visible');
});

// Animación al agregar producto
function animacionAgregar() {
    const carritoBtn = document.getElementById('abrir-carrito');
    carritoBtn.classList.add('agregar');
    setTimeout(() => {
        carritoBtn.classList.remove('agregar');
    }, 500);
}
