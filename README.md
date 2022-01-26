# Jar-micrometer_prometheus

1. Configuración del PrometheusMeterRegistry:

  PrometheusMeterRegistry prometheusMeterRegistry = new PrometheusMeterRegistry(PrometheusConfig.DEFAULT);
  
2. Para crear los contadores:
  CounterPrometheus counterPrometheus = new CounterPrometheus();
  Counter counter = counterPrometheus.createCounter(prometheusMeterRegistry, "nombre.counter");
  
  Nota:Según la documentación de Micrometer la forma de nombrar los contadores, timer, gauge, etc. usa como separador el punto (.).
  
3. La función isTrue:
  counterPrometheus.isTrue(b, counterTrue, counterFalse);
  
  b es un boolean, los contadores counterTrue y counterFalse serán incrementados en función del booleano b.
