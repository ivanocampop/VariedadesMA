<template>
    <div>
        <div id="carouselExampleIndicators" class="carousel slide">
            <div class="carousel-indicators">
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
            </div>
            <div class="carousel-inner">
                <div class="carousel-item active">
                    <div class="w-100 position-relative">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQi02QnB17z0O7N9vqARZwGdakQsRE2iy2bgA&s"
                            class="d-block position-relative top-50 start-50 translate-middle-x vh-100" alt="Nocarga">
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="w-100 position-relative">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQi02QnB17z0O7N9vqARZwGdakQsRE2iy2bgA&s"
                            class="d-block position-relative top-50 start-50 translate-middle-x vh-100" alt="Nocarga">
                    </div>
                </div>
                <div class="carousel-item">
                    <div class="w-100 position-relative">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQi02QnB17z0O7N9vqARZwGdakQsRE2iy2bgA&s"
                            class="d-block position-relative top-50 start-50 translate-middle-x vh-100" alt="Nocarga">
                    </div>
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div>
    </div>
    <br>
    <div>
        <div class="mt-4">
            <div class="text-center w-50 m-auto">
                <h1>Categorias del mes</h1>
                <p>Excepteur sint occaecat cupidatat non proident, sunt in
                    culpa qui officia deserunt mollit anim id est laborum.
                </p>
            </div>
        </div>
    </div>
    <br>
    <div class="row mt-5 w-100 position-absulute">
        <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4 col-xl-4 col-xxl-4">
            <a href="#">
                <img src="data:image/png;base64,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"
                    class="rounded-circle img-thumbnail border position-relative top-0 start-50 translate-middle-x"
                    alt="Nocarga">
            </a>
            <h5 class="text-center mt-4 mb-4">Relojes</h5>
            <p class="text-center">
                <a class="btn btn-success">COMPRAR</a>
            </p>
        </div>
        <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4 col-xl-4 col-xxl-4">
            <a href="#">
                <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMgAAADICAMAAACahl6sAAAAmVBMVEX///8AAAAGAP8sJ//9/f8LBv/29v/X1/9FQf92c/+Vk/+Qjv8kH/8gG/9gXf9mY//c3P86Nv/j4/8UD/8pJP8yLv9KRv+/vv9BPf/r6/9ZVf+Jh//FxP+Miv9+e/+fnf+rqf/Lyv9QTP9raP9xbv+6uf/Qz//y8v+CgP+kov8+Ov/V1P+trP/h4f8xLf95dv+zsv9kYf9WUv8fgWrrAAAGAklEQVR4nO2abVuqTBCAeUbALDENNaQXDTPLzDr9/x/3zAILuwgKsnXmeM394ciZcNkb9k12rP/OBOtvV8AUKGKdASxCDRahBotQg0WowSLUYBFqsAg1WIQaLEINFqEGi1CDRajBItRgEWqwCDVYhBosQg0WoQaLUINFqMEi1GARarAINViEGixCDRahBotQg0WowSLUYBFqsAg1WIQaLEINFqFGDZGnZccBf/Q6y0MfvZ0D4+sn62CoBubKPiriDiDFX8jYpZOGevaB0HFMln1MxI6wAGcabkRBb2nB4soXUx8/nq3K0HGMln1MZC6+vsaDG7yqcyNCQ7xBPRfrcYV/u7UqQjUwWvYxkXF2G+wpwKc4uAZYJqEHgMCqCNXAaNlHRIZ4q9bp8TvADj9cH5y0b9p9gGF5qAZmyz4islVvggcO/rsCCGXkEeCyPCSxLwDu0uNrvZG3LruJCHa06+w//fhir0pptwCD8lDGB97RbnyEVeq4RstuINJdLF7k8Qwrgh84ZN4roVF5KAe79EYMm2tsGNpMYKDs+iIqnzh64Ae2lZss5oBXHlLAjnyFH0uAV+NlnyKCTdr5wM8JQN5APPDLQwo32LiG1j3ezcr57OSym4u42NFgLo46AHmFcAQtD6m8Ya92x7KrmC27oYj95oEcfU64GM53k8oBp2XZjUTuR3gp7yv5T+FZO+UhjRuxvLgob1hty24gMvsjlkSfcu46pUNi4yqfygyUXVvkSTz5P3lhA2UUzYfIYkgHRyx4+KGy64qscM02elECd2nHFNwnM1RJSC9DLG9L+rqJsuuKdP3izwB1er1LunBJSGWGo+ZjOi2aLru2SADwqEdwFefLNj3JFnbFkEqI17eDZFo0XXZdkSdcOhRvZD5FL3AsqgrlYCiwra4jpkXTZdcWeczXrhkfTvp77taX66CSUEYyscftItDqbaDs+iIXoBMHxW/P0XMvgGSBVBGSRGmbsotzooGy64t4ZRezrvbfBpSEEubZGgubkta42pfdQMQpvZjVXY4dpz9QV+UlIcEQG9Z7etzTp/fWZTcR+XdgEWqwCDVYhBosQg0WoQaLUINFqMEi1GARarBIJZ3qPYxW5x6BRSo5G5HX5bL2uaRFmsAi+7BIQpx5sZj64EWL9LVuUrnyZJoXkfnXD1fy67nI+jLyHPCDOyUpsBHtRdzv9CV0MFMrV5JM4y7l++rprCCyyl7N+6viNX5LJATwpoF4tT5x1crtJdPYwngSRqLOk7Um8iS+PgrDjQPFfa1fE8F7uMX6uq+Q7ghmd7mYTHOJD01U0t56MilOnounRvEm9eyiSVKkWREn3bbAesa7lplIIZnG9WGU5jCI7dy43vJc7B3pn4YHttIP0l4ku4GjZK8v78B6Ms0W4EueKlPhchFP7gCtVtX7hIdoL5Jt+M+TBqMMqZGaTINNTG4zi83zOHlOnov34FlNrjuB1iJOtpnWTXaPFREtmQZbf0eC/X9qKed+ia42mL83SH4u0lqknx27SaaoOsmpyTQ7fccw7gn58DtOxt5onj21hpgV6Vi6iJpM09FFJpZ2rn37nJj629NqYrBp4YCz0SqnJ9Ns1AyyFH2Jsl49Ctu/3tnfkvSXvHJ6Ms0A4KP49b21lo3nf59UE4PDb5AkJOWV05Np5kriw9VmE69E5Lm7nUy4STtac8xNiFjROPc7Eykk08xw1ksfybA4IXrZLPietM/mmFiiiHkuXqJ8qpXbS6b5xJEhfg73fZmDJc/FZ7eMh6uXzl7q02+JeF62aBxpi8aomEzjijTM8XcoRqe+tlIWaSrgBOG3+JN32kK+/eq3O9bX5mnlSpJp1lE2iaRtLGuG8ywxZVeVHfzjIpb7MMK1UiQXUknlypNpVoM+nvq9tbVzBcPeBL/RDxenTu4mfiGSgEUSWMQ4LJJwNiJRVP9F78/CGz3UYBFqsAg1WIQaLEINFqEGi1CDRajBItRgEWqwCDVYhBosQg0WoQaLUINFqMEi1GARarAINViEGixCDRahBotQg0WowSLUOC+R8+BsRP4H7V5m1zyMtsgAAAAASUVORK5CYII="
                    class="rounded-circle img-thumbnail position-relative top-0 start-50 translate-middle-x"
                    alt="Nocarga">
            </a>
            <h5 class="text-center mt-4 mb-4">Zapatos</h5>
            <p class="text-center">
                <a class="btn btn-success">COMPRAR</a>
            </p>
        </div>
        <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4 col-xl-4 col-xxl-4">
            <a href="#">
                <img src="data:image/png;base64,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"
                    class="rounded-circle img-thumbnail position-relative top-0 start-50 translate-middle-x"
                    alt="Nocarga">
            </a>
            <h5 class="text-center mt-4 mb-4">Accesorios</h5>
            <p class="text-center">
                <a class="btn btn-success">COMPRAR</a>
            </p>
        </div>
    </div>
    <br>
    <div class="container bg-secondary p-5">
        <div class="row text-center mt-3">
            <div class="w-50 m-auto mb-4">
                <h1>Productos Destacados</h1>
                <p>Reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                    Excepteur sint occaecat cupidatat non proident.
                </p>
            </div>
        </div>
        <div class="row row-cols-1 row-cols-md-3 g-4">
            <div class="col">
                <div class="card">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3_1JlQSbuz0-C8uaCb5z2Xek0qvL2pgerNA&s" class="card-img-top" alt="Nocarga">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                            additional content. This content is a little bit longer.</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3_1JlQSbuz0-C8uaCb5z2Xek0qvL2pgerNA&s" class="card-img-top" alt="Nocarga">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                            additional content. This content is a little bit longer.</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3_1JlQSbuz0-C8uaCb5z2Xek0qvL2pgerNA&s" class="card-img-top" alt="Nocarga">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                            additional content.</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="data:image/png;base64,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" class="card-img-top" alt="Nocarga">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                            additional content. This content is a little bit longer.</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="data:image/png;base64,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" class="card-img-top" alt="Nocarga">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                            additional content. This content is a little bit longer.</p>
                    </div>
                </div>
            </div>
            <div class="col">
                <div class="card">
                    <img src="data:image/png;base64,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" class="card-img-top" alt="Nocarga">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to
                            additional content. This content is a little bit longer.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="container bg-light p-5 w-100">
        <div class="row mt-3 m-auto">
            <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4 col-xl-4 col-xxl-4">
                <h2 class="text-success border-bottom pb-4 fs-3">Tienda variedades M.A</h2>
                <ul class="list-unstyled text-black">
                    <li class="list">123 Se seguirá en la ley 10660</li>
                    <li class="list">010-020-0340</li>
                    <li class="list">info@empresa.com</li>
                </ul>
            </div>
            <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4 col-xl-4 col-xxl-4">
                <h2 class="text-black border-bottom pb-3">Productos</h2>
                <ul class="list-unstyled text-black">
                    <li class="list">lujo</li>
                    <li class="list">Ropa deportiva</li>
                    <li class="list">Zapatos de hombre</li>
                </ul>
            </div>
            <div class="col-xs-4 col-sm-4 col-md-4 col-lg-4 col-xl-4 col-xxl-4">
                <h2 class="text-black border-bottom pb-3">Informacion adicional</h2>
                <ul class="list-unstyled text-black">
                    <li class="list">Hogar</li>
                    <li class="list">Sobre nosotros</li>
                    <li class="list">Ubicaciones de las tiendas</li>
                    <li class="list">Preguntas frecuentes</li>
                </ul>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'ProductClient',
}
</script>