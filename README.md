HTML adicionado: 

<div class="flex">
                    <div class="switch-wrapper flex-2">
                        <legend>Estilo</legend>
                            <label class="switch">
                                <input type="checkbox">
                                <span class="slider"></span>
                            </label>

                            <span class="toogle">Escuro</span>

                    </div>

                    <div class="droparea-wrapper flex-2">

                        <label for="cover-photo">Foto de capa</label>

                            <div class="dropzone">
                                <input type="file" id="cover-photo" name="cover-photo">
                                <img src="assets/icons/upload.svg" alt="ícone de upload">
                                
                                <p>Selecionar</p>
                                
                            </div>
                            

                    </div>
                    </div>

CSS adicionado:
switch.css:

.switch-wrapper {
    
    max-width: 11rem;
   

    legend {
        margin-top: 1.75rem;
        margin-bottom: .75rem;
    }

    .switch {
        position: relative;
        display: inline-block;
        width: 4rem;
        height: 2rem;
    
        outline: 1.5px solid var(--input-stroke);
        border-radius: 999px;
    }

    .toogle {
        display: inline-block;
        text-align: center;
        position: relative;
        left: .75rem;
        transform: translateY(-1rem);
    }

}


.switch input {
    opacity: 0;
    width: 0;
    height: 0;

    
}

.slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: var(--input-base);
    transition: .4s;
    border-radius: 999px;
}

.slider:before {
    position: absolute;
    content: "";
    height: 26px;
    width: 26px;
    left: 4px;
    bottom: 4px;
    background-color: var(--input-stroke);
    transition: .4s;
    border-radius: 50%;
}

input:checked + .slider {
    background-color: var(--input-placeholder);
}

input:checked + .slider:before {
    transform: translateX(26px);
}

.droparea.css:

.droparea-wrapper {
    max-width: 8.5rem;
    margin-top: 1.25rem;
    margin-left: 5rem;
    display: flex;
    flex-direction: column;

    
}

.dropzone {
    display: flex;
    justify-content: center;
    gap: .5rem;
    border-radius: .5rem;
    padding: .75rem;
    text-align: center;
    cursor: pointer;

    margin-top: .50rem;
    
    background-color: var(--input-stroke);

    position: relative;
    .dropzone:hover {
        background-color: var(--brand-light);
    }
    
    .dropzone img {
        max-width: 100px;
        margin-bottom: 10px;
    }

    & input {
        position: absolute;
        opacity: 0;
        inset: 0;
        
        
    }
}

