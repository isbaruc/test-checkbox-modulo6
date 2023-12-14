# Estilando el Checkbox con SVG personalizado

1. crearles un `<div>` (y asignas display: flex) que dentro tendrá el `<input>` y el `<label>`
2. el `<input>` crea una casilla por default, pero como no es esta la que queremos que se vea, pues le agregamos una clase que la oculte que puede quedar de la siguiente forma
   <br>`.visually-hidden {
   position: absolute !important;
   clip: rect(1px 1px 1px 1px);
   padding: 0 !important;
   border: 0 !important;
   height: 0px !important;
   width: 0px !important;
   overflow: hidden;
}`<br>
   <br>💡 Hasta aquí ya no tenemos la casilla sino solo el texto 💡<br><br>
3. Después, al `<label>` a través de una clase le asignaremos el tamaño que tendrá la casilla personalizada y sus demás atributos
   <br><br>:bulb: Nota que usamos ::before ya que pues la casilla va "antes" del texto (y en el label está nuestro texto) :bulb:<br><br>
4. Ahora crearemos en el `<inpu>` una clase (en este caso la nombré modal-form-checkbox ) a la que declararemos los siguientes atributos
   <br>`.modal-form-checkbox:checked + .modal-form-checkbox-label::before {
   background-image: url(./images/iconcheck.svg);
   border-color: #2196f3;
   background-color: #2196f3;
}`<br>
   <br>:bulb: Aquí estamos asignandole que imagen tendrá el fondo de la casilla cuando la el estado sea checked y cual será el elemento que se modifica (::before) :bulb:<br><br>
5. Por último asignaremos los estilos para el acomodo de los elementos
   `.modal-form-checkbox-label {
   display: flex;
   align-items: center;
   font-family: var(--main-font);
   font-weight: normal;
   font-size: 14px;
   line-height: 1.71;
   letter-spacing: 0.03em;
   color: green;
   margin-bottom: 30px;
}`
