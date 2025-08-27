🚩 Reporte de Bugs y Mejoras - [Nombre de la Aplicación]
Tester: [Tu nombre]
Fecha del reporte: [Fecha]
Ambiente de pruebas: [URL del deploy]

🐞 Errores / Bugs encontrados
ID Bug	Descripción breve	Pasos para reproducir	Resultado Esperado	Resultado Obtenido	Severidad	Comentarios adicionales
#1	[Breve y clara descripción del bug]	1. Paso uno
2. Paso dos
3. Paso tres	[¿Qué debería suceder?]	[¿Qué sucede realmente?]	Alta / Media / Baja	[Pantalla, navegador, imágenes, videos]
#2						
#3						

🚀 Oportunidades de mejora / Sugerencias de UX-UI
ID Mejora	Descripción de la mejora	Beneficio esperado	Prioridad	Comentarios adicionales
#M1	[Qué se puede mejorar y cómo hacerlo brevemente]	[¿Qué impacto positivo tendría?]	Alta / Media / Baja	[Opcional: ejemplos visuales, capturas, referencias, etc.]
#M2				
#M3				

🖥️ Contexto de pruebas
Sistema operativo utilizado: [Ej: Windows 11, macOS, Android, iOS]

Navegadores utilizados: [Ej: Chrome versión X, Firefox versión Y, etc.]

Dispositivos utilizados: [Ej: PC escritorio, notebook, smartphone, tablet, etc.]

✅ Observaciones generales
[Espacio para notas adicionales, comentarios generales, recomendaciones, etc.]


<?xml version="1.0" encoding="UTF-8"?>
<jmeterTestPlan version="1.2" properties="5.0" jmeter="5.5">
  <hashTree>
    <TestPlan guiclass="TestPlanGui" testclass="TestPlan" testname="API Creación Campañas - UAT" enabled="true">
      <stringProp name="TestPlan.comments">Plan base: token fijo + IDs numéricos consecutivos por sampler (AtomicLong en PreProcessor).</stringProp>
      <boolProp name="TestPlan.functional_mode">false</boolProp>
      <boolProp name="TestPlan.tearDown_on_shutdown">true</boolProp>
      <boolProp name="TestPlan.serialize_threadgroups">false</boolProp>
      <elementProp name="TestPlan.user_defined_variables" elementType="Arguments" guiclass="ArgumentsPanel" testclass="Arguments" testname="User Defined Variables" enabled="true">
        <collectionProp name="Arguments.arguments">
          <elementProp name="protocol" elementType="Argument">
            <stringProp name="Argument.name">protocol</stringProp>
            <stringProp name="Argument.value">https</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="host" elementType="Argument">
            <stringProp name="Argument.name">host</stringProp>
            <stringProp name="Argument.value">&lt;tu-nodo-uat&gt;</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="port" elementType="Argument">
            <stringProp name="Argument.name">port</stringProp>
            <stringProp name="Argument.value">443</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="createPath" elementType="Argument">
            <stringProp name="Argument.name">createPath</stringProp>
            <stringProp name="Argument.value">/api/campaigns/create</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="accessToken" elementType="Argument">
            <stringProp name="Argument.name">accessToken</stringProp>
            <stringProp name="Argument.value">&lt;PONER_TOKEN_FIJO_AQUI&gt;</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="campaignStart" elementType="Argument">
            <stringProp name="Argument.name">campaignStart</stringProp>
            <stringProp name="Argument.value">1000000</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="internalStart" elementType="Argument">
            <stringProp name="Argument.name">internalStart</stringProp>
            <stringProp name="Argument.value">5000000</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="nameDefault" elementType="Argument">
            <stringProp name="Argument.name">nameDefault</stringProp>
            <stringProp name="Argument.value">UAT-Carga</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
          <elementProp name="descDefault" elementType="Argument">
            <stringProp name="Argument.name">descDefault</stringProp>
            <stringProp name="Argument.value">Prueba performance</stringProp>
            <stringProp name="Argument.metadata">=</stringProp>
          </elementProp>
        </collectionProp>
      </elementProp>
      <stringProp name="TestPlan.user_define_classpath"></stringProp>
    </TestPlan>
    <hashTree>
      <!-- HTTP Request Defaults -->
      <ConfigTestElement guiclass="HttpDefaultsGui" testclass="ConfigTestElement" testname="HTTP Request Defaults" enabled="true">
        <elementProp name="HTTPsampler.Arguments" elementType="Arguments">
          <collectionProp name="Arguments.arguments"/>
        </elementProp>
        <stringProp name="HTTPSampler.domain">${host}</stringProp>
        <stringProp name="HTTPSampler.port">${port}</stringProp>
        <stringProp name="HTTPSampler.protocol">${protocol}</stringProp>
        <stringProp name="HTTPSampler.contentEncoding"></stringProp>
        <stringProp name="HTTPSampler.path"></stringProp>
        <boolProp name="HTTPSampler.concurrentDwn">false</boolProp>
        <stringProp name="HTTPSampler.concurrentPool">6</stringProp>
        <stringProp name="HTTPSampler.connect_timeout"></stringProp>
        <stringProp name="HTTPSampler.response_timeout"></stringProp>
      </ConfigTestElement>
      <hashTree/>
      <!-- Cookie Manager -->
      <CookieManager guiclass="CookiePanel" testclass="CookieManager" testname="HTTP Cookie Manager" enabled="true">
        <collectionProp name="CookieManager.cookies"/>
        <boolProp name="CookieManager.clearEachIteration">false</boolProp>
        <stringProp name="CookieManager.policy">standard</stringProp>
        <boolProp name="CookieManager.allow_variable_cookies">true</boolProp>
      </CookieManager>
      <hashTree/>
      <!-- Thread Group -->
      <ThreadGroup guiclass="ThreadGroupGui" testclass="ThreadGroup" testname="Thread Group" enabled="true">
        <stringProp name="ThreadGroup.on_sample_error">continue</stringProp>
        <elementProp name="ThreadGroup.main_controller" elementType="LoopController" guiclass="LoopControlPanel" testclass="LoopController" testname="Loop Controller" enabled="true">
          <boolProp name="LoopController.continue_forever">false</boolProp>
          <stringProp name="LoopController.loops">2</stringProp>
        </elementProp>
        <stringProp name="ThreadGroup.num_threads">50</stringProp>
        <stringProp name="ThreadGroup.ramp_time">60</stringProp>
        <longProp name="ThreadGroup.start_time">1690000000000</longProp>
        <longProp name="ThreadGroup.end_time">1690000000000</longProp>
        <boolProp name="ThreadGroup.scheduler">false</boolProp>
        <stringProp name="ThreadGroup.duration"></stringProp>
        <stringProp name="ThreadGroup.delay"></stringProp>
      </ThreadGroup>
      <hashTree>
        <!-- Header Manager (token fijo) -->
        <HeaderManager guiclass="HeaderPanel" testclass="HeaderManager" testname="HTTP Header Manager" enabled="true">
          <collectionProp name="HeaderManager.headers">
            <elementProp name="Content-Type" elementType="Header">
              <stringProp name="Header.name">Content-Type</stringProp>
              <stringProp name="Header.value">application/json</stringProp>
            </elementProp>
            <elementProp name="Authorization" elementType="Header">
              <stringProp name="Header.name">Authorization</stringProp>
              <stringProp name="Header.value">Bearer ${accessToken}</stringProp>
            </elementProp>
          </collectionProp>
        </HeaderManager>
        <hashTree/>
        <!-- Uniform Random Timer -->
        <UniformRandomTimer guiclass="UniformRandomTimerGui" testclass="UniformRandomTimer" testname="Uniform Random Timer (200-800ms)" enabled="true">
          <stringProp name="ConstantTimer.delay">200</stringProp>
          <stringProp name="RandomTimer.range">600</stringProp>
        </UniformRandomTimer>
        <hashTree/>
        <!-- Simple Controller: Crear Campaña -->
        <GenericController guiclass="LogicControllerGui" testclass="GenericController" testname="Crear Campaña (solo POST creación)" enabled="true"/>
        <hashTree>
          <!-- HTTP Request - POST Crear Campaña -->
          <HTTPSamplerProxy guiclass="HttpTestSampleGui" testclass="HTTPSamplerProxy" testname="POST ${createPath}" enabled="true">
            <elementProp name="HTTPsampler.Arguments" elementType="Arguments">
              <collectionProp name="Arguments.arguments">
                <elementProp name="" elementType="HTTPArgument">
                  <boolProp name="HTTPArgument.always_encode">false</boolProp>
                  <stringProp name="Argument.value">{&#10;  &quot;campaignId&quot;: ${campaignIdNum},&#10;  &quot;internalId&quot;: ${internalIdNum},&#10;  &quot;name&quot;: &quot;${nameDefault}&quot;,&#10;  &quot;description&quot;: &quot;${descDefault}&quot;,&#10;  &quot;channel&quot;: &quot;EMAIL&quot;,&#10;  &quot;owner&quot;: &quot;UAT&quot;&#10;}</stringProp>
                  <stringProp name="Argument.metadata">=</stringProp>
                </elementProp>
              </collectionProp>
            </elementProp>
            <stringProp name="HTTPSampler.domain">${host}</stringProp>
            <stringProp name="HTTPSampler.port">${port}</stringProp>
            <stringProp name="HTTPSampler.protocol">${protocol}</stringProp>
            <stringProp name="HTTPSampler.contentEncoding"></stringProp>
            <stringProp name="HTTPSampler.path">${createPath}</stringProp>
            <stringProp name="HTTPSampler.method">POST</stringProp>
            <boolProp name="HTTPSampler.follow_redirects">true</boolProp>
            <boolProp name="HTTPSampler.auto_redirects">false</boolProp>
            <boolProp name="HTTPSampler.use_keepalive">true</boolProp>
            <boolProp name="HTTPSampler.DO_MULTIPART_POST">false</boolProp>
            <stringProp name="HTTPSampler.embedded_url_re"></stringProp>
            <stringProp name="HTTPSampler.connect_timeout"></stringProp>
            <stringProp name="HTTPSampler.response_timeout"></stringProp>
            <boolProp name="HTTPSampler.postBodyRaw">true</boolProp>
          </HTTPSamplerProxy>
          <hashTree>
            <!-- JSR223 PreProcessor: IDs numéricos consecutivos globales -->
            <JSR223PreProcessor guiclass="TestBeanGUI" testclass="JSR223PreProcessor" testname="PreProcessor: IDs consecutivos" enabled="true">
              <stringProp name="scriptLanguage">groovy</stringProp>
              <stringProp name="parameters"></stringProp>
              <stringProp name="filename"></stringProp>
              <boolProp name="resetInterpreter">false</boolProp>
              <stringProp name="script">import java.util.concurrent.atomic.AtomicLong

// Inicializa contadores atómicos globales (una vez) a partir de los starts
def initAtomic = { key, startStr -&gt;
    def at = props.getObject(key) as AtomicLong
    if (at == null) {
        long base = 0L
        try {
            base = Long.parseLong(startStr) - 1L
        } catch (Exception e) {
            base = 0L
        }
        at = new AtomicLong(base)
        props.putObject(key, at)
    }
    return at
}

// Lee starts de variables
def campStart = vars.get(&quot;campaignStart&quot;)
def intStart  = vars.get(&quot;internalStart&quot;)

def campAtomic = initAtomic(&quot;campaign.atomic&quot;, campStart)
def intAtomic  = initAtomic(&quot;internal.atomic&quot;, intStart)

// Incrementa UNA vez por request
long nextCamp = campAtomic.incrementAndGet()
long nextInt  = intAtomic.incrementAndGet()

vars.put(&quot;campaignIdNum&quot;, Long.toString(nextCamp))
vars.put(&quot;internalIdNum&quot;, Long.toString(nextInt))
</stringProp>
            </JSR223PreProcessor>
            <hashTree/>
          </hashTree>
        </hashTree>
        <!-- View Results Tree (para debug; desactivar en carga) -->
        <ViewResultsFullVisualizer guiclass="ViewResultsFullVisualizer" testclass="ViewResultsFullVisualizer" testname="View Results Tree" enabled="true"/>
        <hashTree/>
      </hashTree>
    </hashTree>
  </hashTree>
</jmeterTestPlan>
