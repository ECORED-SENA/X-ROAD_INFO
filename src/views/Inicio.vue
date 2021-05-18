<template lang="pug">
section
  BannerPrincipal.mb-5

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p.mb-4 Bienvenido, en este curso los servidores públicos del país se capacitarán con el fin de identificar un diseño metodológico y conceptual en el que se incorpore los elementos de la política de gobierno digital, el marco de interoperabilidad para el estado y el habilitador transversal de los SCD que permita entender el contexto de intercambio de información en el Estado, garantizando a la ciudadanía procesos ágiles, eficientes y transparentes.
    
    p El curso de Gobierno Digital e Interoperabilidad busca que los aprendices reconozcan las características de interoperabilidad, en el marco de la política de gobierno digital y además Identifiquen la herramienta de interoperabilidad para Colombia de acuerdo con el propósito de la política de estrategia de gobierno digital.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
        
    .titulo__template--a.mb-4
      span.h6 2. Justificación<br>del programa
  
    .row
      .col-12.col-md-8.col-lg-9
        p El curso de Gobierno Digital e Interoperabilidad está propuesto con el fin de comprender las necesidades de ofrecer al ciudadano soluciones que garanticen mayor capacidad de atención a los ciudadanos agilizando trámites, información y participación para el ejercicio de sus derechos y mejoramiento de su calidad de vida, de ahí la importancia de la generación de competencias en los servidores públicos del país que permita reconocer el esquema de interoperabilidad, en el marco de la política de gobierno digital para el Estado Colombiano, mediante el uso de software.
      .col-4.col-lg-3.d-none.d-md-block
        figure
          img(src='@/assets/curso/05.png', alt='El instructor - tutor')    


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Competencias<br>a desarrollar

    p  
      span.colorText01
        strong • 
      | Direccionar planes de gestión según marco y modelo estratégico.
  
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4. Perfil<br>de ingreso
    
    p.mb-4 El público objetivo deberá corresponder a los funcionarios públicos del país (funcionarios y contratistas), los cuales estarán principalmente priorizados por:
    
    ul.lista-ul
      li.d-flex  
        i.fas.fa-angle-right
        | Servidores Públicos (funcionarios y Contratistas). 
      li.d-flex  
        i.fas.fa-angle-right
        | CIOs, Lideres TI, Servidores de oficinas TI. 
      li.d-flex  
        i.fas.fa-angle-right
        | Personas que han manifestado el desarrollo de proyectos TI bajo el enfoque de interoperabilidad. 
      li.d-flex  
        i.fas.fa-angle-right
        | Priorizar servidores del ente Territorial sobre ente Nacional de Bogotá. 
      li.d-flex  
        i.fas.fa-angle-right
        | Priorizar funcionarios sobre contratistas.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 6. Estrategia<br>metodológica

    p.mb-4 Centrada en la construcción de autonomía para garantizar la calidad de los procesos formativos   en el marco de la formación por competencias, el aprendizaje por proyectos y el  uso de  técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en el utilización de las tecnologías de la información y la comunicación, integradas, en ambientes abiertos y pluri tecnológicos, que en todo caso recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias.

    p.mb-4 Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el quehacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento.

    .row.g-4.justify-content-center
      .col-5.col-sm-3.col-md-2
        figure.mb-2
          img.w-75.mx-auto(src='@/assets/curso/01.svg', alt='El instructor - tutor')
        p.text-center
          strong El instructor - tutor
      .col-5.col-sm-3.col-md-2
        figure.mb-2
          img.w-75.mx-auto(src='@/assets/curso/02.svg', alt='El instructor - tutor')
        p.text-center
          strong El entorno
      .col-5.col-sm-3.col-md-2
        figure.mb-2
          img.w-75.mx-auto(src='@/assets/curso/03.svg', alt='El instructor - tutor')
        p.text-center
          strong Las TIC

  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos

    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>
