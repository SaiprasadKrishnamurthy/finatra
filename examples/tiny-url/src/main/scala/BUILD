jar_library(name='jedis',
  jars = [
    jar(org='redis.clients', name='jedis', rev='2.7.2'),
  ]
)

scala_library(
  name='scala',
  dependencies=[
    ':jedis',
    '3rdparty/jvm/ch/qos/logback:logback-classic',
    '3rdparty/jvm/com/google/inject:guice',
    '3rdparty/jvm/javax/inject:javax.inject',
    'finatra/slf4j',
    'finatra/http',
  ],
  excludes = [
    exclude(org='org.slf4j', name='slf4j-jdk14')
  ],
  sources=rglobs('*.scala'),
  resources=[
    'finatra/examples/tiny-url/src/main/resources'
  ]
)
