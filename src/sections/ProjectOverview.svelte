<script>
  import { slide } from "svelte/transition";
  import SubHeader from "../SubHeader.svelte";

  let showMore = false;
  $: arrowDirection = showMore ? "down" : "right";

  function toggleShowMore() {
    showMore = !showMore;
  }
</script>

<style>
  img {
    max-width: 100%;
  }

  p.intro {
    text-align: center;
  }

  .project-card {
    padding-top: 5px;
    padding-bottom: 5px;
    margin-top: 30px;
    margin-left: 50px;
    margin-right: 50px;
    box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.2),
      0 4px 20px 0 rgba(0, 0, 0, 0.19);
  }

  .project-title {
    font-size: 20px;
    font-style: italic;
    font-weight: bold;
  }

  .project-subtitle {
    font-style: italic;
  }

  .see-more {
    text-align: center;
  }

  button.see-more-button {
    border: none;
    background: none;
    margin: 20px;
    cursor: pointer;
  }

  button.see-more-button:focus {
    outline: 0;
  }

  .grade {
    text-align: right;
    font-size: 17px;
    font-weight: bold;
  }

  .year {
    margin-top: 35px;
    text-align: center;
    font-weight: 600;
  }

  @media only screen and (min-width: 1300px) {
    .section {
      padding: 30px 220px;
    }
  }

  @media only screen and (max-width: 900px) {
    .section {
      padding-right: 0;
      padding-left: 0;
    }

    .project-card {
      margin-left: 20px;
      margin-right: 20px;
    }

    .project-card.project-card-last {
      margin-bottom: 30px;
    }
  }
</style>

<div id="Projects" />
<SubHeader className="header-image" title="Projects" />
<div class="section">
  <p class="intro">
    Here are some examples of projects I undertook in my time at Edinburgh
    Napier University.
  </p>
  <h3 class="year">4th Year</h3>

  <div class="w3-row w3-container project-card">
    <div class="w3-col m6 w3-left">
      <img
        src="/images/ProjectEvaluation/BirdsEyeView.PNG"
        title="Site Plan"
        alt="Site Plan" />
      <img
        src="/images/ProjectEvaluation/HousePlan.PNG"
        title="House Plans"
        alt="House Plans" />
    </div>
    <div class="w3-col m6 w3-padding-large">
      <div class="project-title">Project Evaluation</div>
      <div class="grade">Grade A+</div>
      <p>
        This was a three-month long project where I worked in an
        inter-disciplinary team of 12 prople including Architectural
        Technologists, Construction managers, Building Surveyors, Quantity
        Surveyors and Real Estate Surveyors.
      </p>
      <p>
        The task was to provide designs for Taylor Wimpey for a development site
        in Maybury, Edinburgh. The development was too include a mixture of
        residential buildings, with 40% Gold standard and 60% Silver of the
        Scottish Building Standards Section 7 Sustainability and commercial
        units and to outline the constraints and opportunities. As a team we
        were also to retain the existing farmhouse at the centre of the site
        through appropriate retrofit.
        <b>
          My team was voted as the winning team on this project by a panel of
          representitives from Taylor Wimpey.
        </b>
      </p>
      <p>PDFs of some of the work from me and the team:</p>
      <p>
        <a href="/ProjectEvaluation/SVG-DRW-A-002.pdf">Site plan</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-006.pdf">Sun analysis</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-007.pdf">House plans</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-009.pdf">House plans (2)</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-014.pdf">Conceptual view</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-016.pdf">Conceptual view (2)</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-021.pdf">Community space plans</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-022.pdf">Conceptual graphics</a>
        |
        <a href="/ProjectEvaluation/SVG-DRW-A-026.pdf">
          Conceptual graphics (2)
        </a>
      </p>
    </div>
  </div>

  <div class="w3-row w3-container project-card">
    <div class="w3-col m6 w3-padding-large">
      <div class="project-header">
        <div class="project-title">Architectural Practice and Management</div>
        <div class="grade">Grade A+</div>
      </div>
      <p>
        For this project the brief was to assume the role of a Technical
        Director responsible for design and project management for my practice.
        The project was a five star boutique hotel located in Edinburgh. I was
        to prepare a report to a Board of Directors and an outline bid. Within
        the report I was to include risk analysis, costing, Gantt charts for
        duration of tasks and clear alliance with the CIAT codes. Alongside the
        report a full redesign of the previously proposed hotel design was to be
        completed which I carried out on Revit.
      </p>
    </div>
    <div class="w3-col m6 w3-padding-large">
      <div class="project-header">
        <div class="project-title">Sustainable Development</div>
        <div class="grade">Grade B</div>
      </div>
      <p>
        During this module I studied; Energy and environmental issues, renewable
        technologies, low energy buildings and carbon footprint. Utilising class
        taught lecturers, topical news casting and further reading to ultimately
        put everything together into a 3 hour examination.
      </p>
    </div>
  </div>

  <div class="w3-row w3-container project-card">
    <div class="w3-col m6 w3-left">
      <img
        src="/images/year4/(AT4)_Library_Visual.png"
        title="Site Plan"
        alt="Site Plan" />
      <img
        src="/images/year4/(AT4)_3D_Site_Plan.png"
        title="House Plans"
        alt="House Plans" />
    </div>
    <div class="w3-col m6 w3-padding-large">
      <div class="project-header">
        <div class="project-title">Architectural Technology 4</div>
        <div class="grade">Grade B</div>
      </div>
      <p>
        This project was a culmination of the design elements of my trimester 1
        of my final year in ‘Project Evaluation.’ and my overall programme. This
        project was to provide a Domestic and a Non-Domestic solution
        encompassing off-site approaches where possible, retrofit and
        sustainable approaches where possible and provide technical solutions
        aligned to the Technical Standards Domestic / Non-Domestic as of
        December 2019. My choice of Non-Domestic was a retrofit of the existing
        Farmhouse with a new extension and my Domestic build within the site was
        a two storey apartment complex designed around a ‘lifetime home.’
      </p>
      <p>
        For my final submission I utilised a combination of the programmes I
        have used over the last 5/6 years including: Revit, AutoCAD, InDesign,
        Build Desk-U and Photoshop
      </p>
      <p>PDFs of some of the work from me and the team:</p>
      <p>
        <a href="/AT4/(AT4)_Farmhouse_Elevations.pdf">Farmhouse Elevations</a>
        |
        <a href="/AT4/(AT4)_Farmhouse_Fire_Resistance.pdf">
          Farmhouse Fire Resistance
        </a>
        |
        <a href="/AT4/(AT4)_Farmhouse_Floor_Plans.pdf">Farmhouse Floor Plans</a>
        |
        <a href="/AT4/(AT4)_Farmhouse_GF_to_Eaves_Section.pdf">
          Farmhouse GF to Eaves Section
        </a>
        |
        <a href="/AT4/(AT4)_Farmhouse_Retrofit_GF_to_Eaves_Section.pdf">
          Farmhouse Retrofit GF to Eaves Section
        </a>
        |
        <a href="/AT4/(AT4)_Flats_Elevations.pdf">Flats Elevations</a>
        |
        <a href="/AT4/(AT4)_Flats_External_Wall_GF_to_Eaves_Section.pdf">
          Flats External Wall GF to Eaves Section
        </a>
        |
        <a href="/AT4/(AT4)_Flats_Fire_Resistance.pdf">Flats Fire Resistance</a>
        |
        <a href="/AT4/(AT4)_Flats_Floor_Plans.pdf">Flats Floor Plans</a>
        |
        <a href="/AT4/(AT4)_Flats_Separating_Wall_GF_to_Eaves_Section.pdf">
          Flats Separating Wall GF to Eaves Section
        </a>
      </p>
    </div>
  </div>

  <div class="see-more">
    <button class="see-more-button" on:click={toggleShowMore}>
      See previous years
      <i class={`fa fa-arrow-${arrowDirection}`} />
    </button>
  </div>

  {#if showMore}
    <h3 class="year">Third Year</h3>

    <div class="w3-row w3-container project-card">
      <div class="w3-col m6 w3-left">
        <img src="/images/AT3/EastElevation.jpg" alt="East elevation" />
        <img
          src="/images/AT3/SouthElevation.jpg"
          alt="Provided area for the new kindergarten" />
      </div>
      <div class="w3-col m6 w3-padding-large">
        <div class="project-title">Architectural Technology 3</div>
        <div class="project-subtitle">Vintage Car Parts Garage</div>
        <p>
          The task in this project was to propose a scheme design to relocate an
          existing Vintage and Veteran Car Parts garage to larger premises to
          allow the business to expand and increase the capacity for
          manufacturing rare parts.
        </p>
        <p>
          As well as having a showroom and sales counter the requirements asked
          for the existing industrial unit to be converted to provide
          accommodation for storage areas, offices, spaces for manufacturing and
          fitting car parts and a space for designing new car parts.
        </p>
      </div>
    </div>

    <div class="w3-row w3-container project-card" transition:slide>
      <div class="w3-col m6 w3-padding-large">
        <div class="project-title">Building Control and Fire Engineering</div>
        <div class="grade">Grade B</div>
        <p>
          For this submission I was asked to propose a scheme design to create a
          garage to accomodate for a 'snow cat' with lobby, wc, store, upper
          lounge, terrace and grass roof area.
        </p>
        <p>
          The learning outcomes of this project were to demonstrate knowledge of
          building control procedures, warrant application, fees and
          enforcement: analysing technical information on building component
          details and drawings for compliance with technical handbooks. I also
          completed a building warrant portfolio comprising of drawings,
          details, costings and reports.
        </p>
      </div>
      <div class="w3-col m6 w3-padding-large">
        <div class="project-title">Building Engineering 3</div>
        <div class="grade">Grade B</div>
        <p>
          In this project I calculated values such as silencer attenuation,
          sound pressure, volumetric flow rate of air and heat energy using a
          duct systems workbook. Answering all of the appropriate coursework
          questions resulting in a complete workbook with calculations for the
          sound attenuation for a doctors consulting room in a hospital and any
          alterations in order to reduce any noise disruption
        </p>
      </div>
    </div>
    <div class="w3-row w3-container project-card" transition:slide>
      <div class="w3-col m6 w3-padding-large">
        <div class="project-title">Contract Administration and Practice</div>
        <div class="grade">Grade B</div>
        <p>
          In this project I evaluated matrix scoring, procurement routes and
          evaluate clauses under JCT2011 SBC/Q/Scot.
        </p>
        <p>
          Creating a scenario of a medium sized building contract on a site I
          had to evaluate clauses within the JCT2011 SBC/Q/Scot and compare and
          contrast the respective positions of the SBCC 2011 Standard Building
          Contract with Quantities for use in Scotland and the NEC3 Engineering
          and Construction Contract.
        </p>
      </div>
    </div>

    <h3 class="year">Second Year</h3>

    <div class="w3-row w3-container project-card project-card-last">
      <div class="w3-col m6 w3-left">
        <img
          src="/images/CW2/Picture2.png"
          title="Provided area for the new kindergarten."
          alt="Provided area for the new kindergarten" />
      </div>
      <div class="w3-col m6 w3-padding-large">
        <div class="project-title">Architectural Technology 2</div>
        <div class="project-subtitle">Waterfall Kindergarten</div>
        <div class="grade">Grade A+</div>
        <p>
          This was a trimester-long project which involved designing a
          kindergarten to be built in an existing area of land in Edinburgh. It
          was carried out over 4 coursework assignments, in which the tasks
          ranged from research, to designing, to developing renderings.
        </p>
      </div>
    </div>
  {/if}
</div>
