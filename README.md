Este es el repositorio del backend del curso de angular 19 con .Net 9

Crear un proyecto asp.Net Core 

Para que corra swagger hay que habilitar 2 paquetes de nuguet
** Swashbuckle.AspNetCore

En program.cs

modificar el //builder.Services.AddOpenApi();

Agregar las siguientes lineas
builder.Services.AddEndpointsApiExplorer();
builder.Services.AddSwaggerGen();

Dentro de la condicion IsDevelopment Agreggar las lineas UserSwagger y Us SwaggerUI

if (app.Environment.IsDevelopment())
{
    //app.MapOpenApi();
    app.UseSwagger();
    app.UseSwaggerUI();
}
