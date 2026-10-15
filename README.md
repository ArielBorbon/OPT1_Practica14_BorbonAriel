## Ariel Eduardo Borbon Izaguirre 252116

¿por qué en la pestaña Red salen dos peticiones al cargar?
es por el strictmode de react, cuando esta en modo dev, react arma y desarma los componentes para detectar errores de limpieza, pero ya en un entorno de produccion esto se deja de hacer

¿qué pasa si quitas el arreglo de dependencias del efecto? 
se ejecutaria en cada renderizado del componente, en lugar de hacerse solo al inicio, si se actualizaria un estado, crearia un cambio renderizado, el cual se llamaria a si mismo, haciendo un bucle infinito

¿qué hace e.preventDefault() y qué pasa si lo quitas?
detiene el comportamiento que tiene el navegador a un evento, por ejemplo en un formulario hace que la pagina no se recargue cuando se presiona enviar, si se quita el navegador refrescaria la pagina al instante, perdiendo todos los estados temporales que teniamos 
