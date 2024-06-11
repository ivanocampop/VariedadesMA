<template>
    <div>
        <div class="row row-cols-2 g-2 needs-validation" novalidate>
            <div class="col-xs-12 col-md-6">
                <label for="nombre" class="form-label">Nombres</label>
                <input type="text" class="form-control" id="nombres" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="apellidos" class="form-label">Apellidos</label>
                <input type="text" class="form-control" id="apellidos" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="nickname" class="form-label">Nickname</label>
                <input type="text" class="form-control" id="nickname" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="clave" class="form-label">Clave</label>
                <input type="password" class="form-control" id="clave" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="correo" class="form-label">Correo</label>
                <input type="email" class="form-control" id="correo" required>
                    <div class="valid-feedback">
                        Bien!
                    </div>
                    <div class="invalid-feedback">
                        El campo no puede quedar vacio!.
                    </div>
                
            </div>
            <div class="col-md-6">
                <label for="validationCustomTelefono" class="form-label">Telefono</label>
                <input type="number" class="form-control" id="validationCustomTelefono" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="validationCustomEstado" class="form-label">Estado</label>
                <select class="form-select" id="validationCustomEstado" required>
                    <option selected disabled value="">Elegir...</option>
                    <option value="1">Activo</option>
                    <option value="2">Inactivo</option>
                </select>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    Seleccione el estado!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="validationCustomAdmin" class="form-label">Admin</label>
                <select class="form-select" id="validationCustomAdmin" required>
                    <option selected disabled value="">Elegir...</option>
                    <option value="1">Si</option>
                    <option value="2">No</option>
                </select>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    Seleccione el estado!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="validationCustomClaveCaja" class="form-label">Clave Caja</label>
                <input type="password" class="form-control" id="validationCustomClaveCaja" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-6">
                <label for="validationCustomRol" class="form-label">Rol</label>
                <select class="form-select" id="validationCustomRol" required>
                    <option selected disabled value="">Elegir...</option>
                    <option value="1">Admin</option>
                    <option value="2">Empleado</option>
                </select>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-md-12">
                <label for="validationCustomEmpresa" class="form-label">Empresa</label>
                <input type="text" class="form-control" id="validationCustomEmpresa" required>
                <div class="valid-feedback">
                    Bien!
                </div>
                <div class="invalid-feedback">
                    El campo no puede quedar vacio!.
                </div>
            </div>
            <div class="col-12">
                <div class="form-check">
                    <input class="form-check-input" type="checkbox" value="" id="invalidCheck" required>
                    <label class="form-check-label" for="invalidCheck">
                        Agree to terms and conditions
                    </label>
                    <div class="invalid-feedback">
                        You must agree before submitting.
                    </div>
                </div>
            </div>
            <div class="col-12">
                <button class="btn btn-primary" type="submit">Submit form</button>
            </div>
            <hr>
            <div class="row g-2">
                <div class="col">
                    <input type="text" class="form-control" placeholder="First name" aria-label="First name">
                </div>
                <div class="col">
                    <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
                </div>
            </div>
            <div class="row g-3">
                <div class="col">
                    <input type="text" class="form-control" placeholder="First name" aria-label="First name">
                </div>
                <div class="col">
                    <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
                </div>
            </div>
        </div>

    </div>
</template>
<script>
export default {
    name: 'FormUser',
}
</script>