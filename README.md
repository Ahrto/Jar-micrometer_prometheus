# Jar-micrometer_prometheus

<b>1. Configuración del PrometheusMeterRegistry:</b>

  PrometheusMeterRegistry prometheusMeterRegistry = new PrometheusMeterRegistry(PrometheusConfig.DEFAULT);
  
<b>2. Para crear los contadores:</b><br>
  CounterPrometheus counterPrometheus = new CounterPrometheus();
  Counter counter = counterPrometheus.createCounter(prometheusMeterRegistry, "nombre.counter");
  
  <b>Nota:</b>Según la documentación de Micrometer la forma de nombrar los contadores, timer, gauge, etc. usa como separador el punto (.).
  
<b>3. La función isTrue:</b><br>
  counterPrometheus.isTrue(b, counterTrue, counterFalse);
  
  b es un boolean, los contadores counterTrue y counterFalse serán incrementados en función del booleano b.
