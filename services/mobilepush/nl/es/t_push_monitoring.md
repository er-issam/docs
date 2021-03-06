---

copyright:
 years: 2015, 2017

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen:.screen}
{:codeblock:.codeblock}

# Supervisión para notificaciones push 
{: #monitor-notifications}
Última actualización: 12 de abril de 2017
{: .last-updated}


El servicio {{site.data.keyword.mobilepushshort}} de IBM ahora amplía sus funciones para supervisar el rendimiento push generando gráficos desde los datos de usuario. Puede utilizar el programa de utilidad para enumerar todas las notificaciones push enviadas, o para enumerar todos los dispositivos registrados y para analizar información de forma diaria, semanal o mensual.

Para generar informes para todas las notificaciones enviadas, utilice el método de informes Push Messages GET en [API REST](https://mobile.{DomainName}/imfpush/){: new_window}. 

![Informe de notificaciones enviadas](images/monitoring_messages.jpg)


Para generar informes para todos los dispositivos registrados, utilice el método de informes Push Device Registrations GET en [API REST](https://mobile.{DomainName}/imfpush/){: new_window}.

![Informe de dispositivos registrados](images/monitoring_devices.jpg)

Para obtener información sobre cómo actualizar el SDK de Android para que supervise información sobre notificaciones, consulte el tema sobre 'Supervisión de notificaciones push en dispositivos Android' en [Habilitación de notificaciones para dispositivos móviles](c_enable_push.html).


 
