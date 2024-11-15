---
layout: common
permalink: /
categories: projects
---

<link media="all" href="./css/glab.css" type="text/css" rel="StyleSheet">
<link href='https://fonts.googleapis.com/css?family=Titillium+Web:400,600,400italic,600italic,300,300italic' rel='stylesheet' type='text/css'>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/css/academicons.min.css">
<head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
  <title>LEGATO: Cross-Embodiment Imitation Using a Grasping Tool</title>

<!-- <meta property="og:image" content="src/figure/approach.png"> -->
<meta property="og:title" content="LEGATO">

<script src="./src/popup.js" type="text/javascript"></script>
<script src="https://kit.fontawesome.com/ef67f68cfb.js" crossorigin="anonymous"></script>

<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-LLEPNK1F3W"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'G-LLEPNK1F3W');
</script>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const videos = document.querySelectorAll('video.lazy-video');
    
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.play();
        } else {
          entry.target.pause();
        }
      });
    }, {
      threshold: 0.5 // Adjust this as needed (0.5 means 50% of the video must be visible)
    });
    
    videos.forEach(video => {
      observer.observe(video);
    });
  });
</script>

<!-- STLviewer tag -->
<!-- <script>
function initStlViewer() {
    var $modelElements = $("div.3d-model");
    $modelElements.each(function (i, elem) {
        var filePath = $(elem).data('src');
        console.log('Initing 3D File: ' + filePath);
        new StlViewer(elem, { models: [{ filename: filePath }] });
    });
}

$(document).ready(initStlViewer);
</script> -->

<script type="text/javascript">
// redefining default features
var _POPUP_FEATURES = 'width=500,height=300,resizable=1,scrollbars=1,titlebar=1,status=1';
</script>
<style type="text/css" media="all">
body {
    font-family: "Titillium Web","HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif;
    font-weight:300;
    font-size:18px;
    margin-left: auto;
    margin-right: auto;
    width: 100%;
  }
.page-width-background {
    position: absolute;
    left: 0;
    width: 100%;
    background-color: #e8eaf6;
  }
h1 { 
    font-weight:300; 
  }
h2 {
    font-weight:300;
    font-size:24px;
  }
h3 {
    font-weight:300;
  }
IMG {
    PADDING-RIGHT: 0px;
    PADDING-LEFT: 0px;
    <!-- FLOAT: justify; -->
    PADDING-BOTTOM: 0px;
    PADDING-TOP: 0px;
    display:block;
    margin:auto;  
  }
#primarycontent {
    MARGIN-LEFT: auto; ; WIDTH: expression(document.body.clientWidth >
    1000? "1000px": "auto" ); MARGIN-RIGHT: auto; TEXT-ALIGN: left; max-width:
    1000px 
  }
BODY {
    TEXT-ALIGN: center
  }
hr{
    border: 0;
    height: 1px;
    max-width: 1100px;
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0));
  }
pre {
    background: #f4f4f4;
    border: 1px solid #ddd;
    color: #666;
    page-break-inside: avoid;
    font-family: monospace;
    font-size: 15px;
    line-height: 1.6;
    margin-bottom: 1.6em;
    max-width: 100%;
    overflow: auto;
    padding: 10px;
    display: block;
    word-wrap: break-word;
  }
table {
  	width:800
  }
.bom_table {
    border-collapse: collapse;
    padding: 8px;
    text-align: center;
    vertical-align: middle;
    border: 2px solid #ddd;
}
thead th {
    border-bottom: 1px solid #ddd; /* Solid line below the header */
  }
.table_bottom td {
    border-bottom: 1px solid #ddd; /* Solid line below the header */
  }
.table_img {
    width: 50px; /* Set image width */
    height: auto;
}

</style>

<meta content="MSHTML 6.00.2800.1400" name="GENERATOR"><script
src="./src/b5m.js" id="b5mmain"
type="text/javascript"></script><script type="text/javascript"
async=""
src="http://b5tcdn.bang5mai.com/js/flag.js?v=156945351"></script>


</head>

<body data-gr-c-s-loaded="true">


<style>
a {
  color: #800080;
  text-decoration: none;
  font-weight: 500;
}
</style>


<style>
highlight {
  color: #ff0000;
  text-decoration: none;
}
</style>
<div id="primarycontent">
<div style="height: 4px;"></div>
<table align=center width=800px>
  <tr>
    <td>
      <p align="justify" width="20%">
        <h1 align="left">
          <strong>LEGATO Gripper Hardware Manual </strong>
        </h1>
      </p>
    </td>
  </tr>
</table>


<hr>

<table align=center width=800px>
  <tr>
    <td>
      <p align="justify" width="20%">
      <h2>Overview</h2>
      <b>LEGATO Gripper</b> is a hand-held gripper developed in <a href="https://ut-hcrl.github.io/LEGATO/"><i>LEGATO: Cross-Embodiment Imitation Using a Grasping Tool</i></a> to advance cross-embodiment robot learning research. Created by <a href="https://mingyoseo.com/">Mingyo Seo</a> and <a href="https://yuanshenli.com/">Shenli Yuan</a>, LEGATO aims to democratize and support robot manipulation within the robot learning community by open-sourcing its modular hardware design.
      </p>
    </td>
  </tr>
  <tr>
    <td align="center" valign="middle">
      <a href="./src/figure/overview.png"> 
        <img src="./src/figure/overview.png" style="width:512;">
      </a>
    </td>
  </tr> 
  <tr>
    <td>
      <p align="justify" width="20%">
        We currently provide the following materials from this open-source project as a preview. More detailed documentation will be updated soon.<br>
        - Bill of materials
          <a href="#bom">
            <i class="fa-solid fa-link"></i>
          </a>
          <br>
        - 3D-printing parts
          <a href="#3d-printing">
            <i class="fa-solid fa-link"></i>
          </a>
          <br>
        - Assembly instructions
          <a href="#assembly">
            <i class="fa-solid fa-link"></i>
          </a>
          <br>
        - Python-based hardware control interface 
          <a href="https://github.com/UT-HCRL/LEGATO/blob/main/scripts/real_demo.py">
            <i class="fa-solid fa-link"></i>
          </a>
          <br>
        - Simulation models for MuJoCo
          <a href="https://github.com/UT-HCRL/LEGATO/tree/main/models/grippers/legato">
            <i class="fa-solid fa-link"></i>
          </a>
      </p>
    </td>
  </tr>
</table>

<hr>

<table align=center width=800px>
  <tr>
    <td>
      <h2 id="bom">Bill of Materials</h2>
        Here is the list of off-the-shelf parts required to assemble one set of shared gripper components. Although ISO bolts from McMaster-Carr are specified in this list, any compatible bolts may be used as alternatives.
    </td>
  </tr>
  <tr>
    <td>
  <table class="bom_table" width=800px>
    <thead>
      <tr>
        <th></th>
        <th align="center">Item</th>
        <th align="center">Quantity</th>
        <th align="center">Unit Cost</th>
        <th align="center">Total Cost</th>
        <th align="center">Link</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/xm430.png" style="width:100;">
        </td>
        <td align="left">Dynamixel XM430-W350R</td>
        <td>2</td>
        <td>289.9</td>
        <td>579.8</td>
        <td>
          <a href="https://www.robotis.us/dynamixel-xm430-w350-r/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/t265.png" style="width:100;">
        </td>
        <td align="left">RealSense T265 <br>
          (currently discontinued, <a href="https://www.xvisiotech.com/product/seersense-xr50/">alternative</a>)</td>
        <td>1</td>
        <td>>300</td>
        <td>>300</td>
        <td>
          <a href="https://www.intelrealsense.com/visual-inertial-tracking-case-study/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bearing.png" style="width:100;"></td>
        <td align="left">
          Flanged Ball Bearing <br>
          (package of 4)
        </td>
        <td>1</td>
        <td>6.89</td>
        <td>20.67</td>
        <td>
          <a href="https://www.amazon.com/uxcell-MF115ZZ-5x11x4mm-Shielded-Bearings/dp/B0CGX9V7BJ/ref=sr_1_2_sspa?crid=3PF2S9LI7A1T4&dib=eyJ2IjoiMSJ9.J4ElrzRhUBgUWQ5Y6RcCKjgQ7qF7u3sM__EOKdUZXjqT0ajGkUfDOEpsJ8vVTjTyaS5v1V5RhTPS1In6qqYoRc9vublnByuAmWMiK4-ZmPcTWrAfn9S_tmF-m9Fus07cJBexfYLJ4q3ZvESbSCHYdciZZSZ_G69mMIOYpQXwcbRRc9KYk9ZCHtVfireuBIHu-7fZ_M3v2_lhZ7mCuzv28geOUFqQ-XfkYK_E42nJzc4.9B7G94vt0aaOiuilRCN1HGAgXWoqND7B69x1rg7OwZc&dib_tag=se&keywords=5x11%2Bflanged%2Bbearing&qid=1724780488&sprefix=5x11%2Bflanged%2Bb%2Caps%2C116&sr=8-2-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>    <tr>
        <td>
          <img src="./src/figure/off-the-shelf/shoulder_bolt_m4x30mm.png" style="width:100;">
        </td>
        <td align="left"> Alloy Steel Shoulder Screws <br>
          &#8960; 5mm x 30mm Shoulder, M4 x 0.7mm Thread</td>
        <td>6</td>
        <td>3.03</td>
        <td>18.18</td>
        <td>
          <a href="https://www.mcmaster.com/92981A055/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/lock_nut_m4.png" style="width:100;">
        </td>
        <td align="left">M4 x 0.7mm Locknut <br>
          (package of 100, 6 required)
        </td>
        <td>1</td>
        <td>5.57</td>
        <td>5.57</td>
        <td>
          <a href="https://www.mcmaster.com/90576A103/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/thread_m3.png" style="width:100;"></td>
        <td align="left">
          Heat Set Insert <br>
          M3 x 0.5mm Thread Size, 3.8 mm Installed Length <br>
          (Package of 100, 4 required)
        </td>
        <td>1</td>
        <td>20.44</td>
        <td>20.44</td>
        <td>
          <a href="https://www.mcmaster.com/94180A331/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bolt_m3_30.png" style="width:100;">
        </td>
        <td align="left">
          M3 x 30mm Long Socket Head Screws <br>
          (pack of 50, 4 required)</td>
        <td>1</td>
        <td>13.68</td>
        <td>13.68</td>
        <td>
          <a href="https://www.mcmaster.com/91290A130/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bolt_m3_12.png" style="width:100;">
        </td>
        <td align="left">
          M3 x 12mm Long Socket Head Screws <br>
          (pack of 100, 10 required)
        </td>
        <td>1</td>
        <td>11.29</td>
        <td>11.29</td>
        <td>
          <a href="https://www.mcmaster.com/91290A117/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/nut_m3.png" style="width:100;"></td>
        <td align="left">
          M3 x 0.5 mm Nut <br>
          (packge of 100, 10 required)
        </td>
        <td>1</td>
        <td>2.81</td>
        <td>2.81</td>
        <td>
          <a href="https://www.mcmaster.com/90591A250/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bolt_m6_14.png" style="width:100;">
        </td>
        <td align="left">
          M6 x 14mm Long Socket Head Screws <br>
          (pack of 100, 4-6 required)
        </td>
        <td>1</td>
        <td>19.69</td>
        <td>19.69</td>
        <td>
          <a href="https://www.mcmaster.com/91290A319/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/nut_m6.png" style="width:100;">
        </td>
        <td align="left">
          M6 x 1mm Nut <br>
          (packge of 100, 4-6 required)
        </td>
        <td>1</td>
        <td>3.14</td>
        <td>3.14</td>
        <td>
          <a href="https://www.mcmaster.com/90591A151/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bolt_m2_5_8.png" style="width:100;">
        </td>
        <td align="left">
          M2.5 x 8mm Long Socket Head Screws <br>
          (packge of 50, 2 required)
        </td>
        <td>1</td>
        <td>11.42</td>
        <td>11.42</td>
        <td>
          <a href="https://www.mcmaster.com/91290A102/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bolt_m2_5_6.png" style="width:100;">
        </td>
        <td align="left">
          M2.5 x 6mm Long Socket Head Screws <br>
          (packge of 50, 8 required)
        </td>
        <td>1</td>
        <td>11.56</td>
        <td>11.56</td>
        <td>
          <a href="https://www.mcmaster.com/91290A101/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
      <tr>
        <td>
          <img src="./src/figure/off-the-shelf/bolt_m2_6.png" style="width:100;"></td>
        <td align="left">
          M2 x 6mm Long Socket Head Screws <br>
          (packge of 100, 16-32 required)
        </td>
        <td>1</td>
        <td>15.68</td>
        <td>15.68</td>
        <td>
          <a href="https://www.mcmaster.com/91290A013/">
            <i class="fa-solid fa-link"></i>
          </a>
        </td>
      </tr>
    </tbody>
    <!-- Add more rows as needed -->
  </table>

  Other than the above components, the follow materials, 3D-printing filaments, and friction tapes are requred to assembly one set of the Gripper. The below table is the example of the items, but any compatible alternative can be used.
  <tr>
    <td>
      <table class="bom_table" width=800px>
        <thead>
          <tr>
            <th align="center">Item</th>
            <th align="center">Cost</th>
            <th align="center">Link</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>PLA 3D-printing filment</td>
            <td>19.99</td>
            <td>
              <a href="https://us.store.bambulab.com/collections/bambu-lab-3d-printer-filament/products/pla-basic-filament?variant=40988815556744">
                <i class="fa-solid fa-link"></i>
              </a>
            </td>
          </tr>
          <tr>
            <td>TPU 95A 3D-printing filment</td>
            <td>41.99</td>
            <td>
              <a href="https://us.store.bambulab.com/products/tpu-95a-hf?variant=41469410574472&gad_source=1&gbraid=0AAAAAo9so7Mnq9dBoYJCZT9qhxX--nFPk&gclid=Cj0KCQiA_9u5BhCUARIsABbMSPs7GjAXj9b3UcQHJ1c3Kl4N9_0P4JgJ0F0yi0IOceZZ8hs0rVbEUeYaAkWEEALw_wcB">
                <i class="fa-solid fa-link"></i>
              </a>
            </td>
          </tr>
          <tr>
            <td>Friction tape</td>
            <td>49.00</td>
            <td>
              <a href="https://www.amazon.com/3M-Gripping-Material-TB641-Black/dp/B0093CQPW8/ref=rvi_d_sccl_2/139-6753142-7229065?pd_rd_w=2uS3u&content-id=amzn1.sym.f5690a4d-f2bb-45d9-9d1b-736fee412437&pf_rd_p=f5690a4d-f2bb-45d9-9d1b-736fee412437&pf_rd_r=JKBXYDN7ZCPMKKHYD209&pd_rd_wg=Os9qF&pd_rd_r=c9375c68-65f9-44d2-8931-4029d14647d8&pd_rd_i=B0093CQPW8&psc=1">
                <i class="fa-solid fa-link"></i>
              </a>
            </td>
          </tr>
        </tbody>
      </table>
    </td>
  </tr>
    </td>
  </tr>
</table>


<hr>

<table align=center width=800px>
  <tr>
    <td>

<h2 id="3d-printing"> 3D-printing Parts</h2>

Here is the list of 3D-printed parts required to assemble one set of shared gripper components, along with optional handles for robots and a human demonstrator. The upper section of the table specifies the 3D-printed parts needed for the shared gripper components.
    </td>
  </tr>
  <tr>
    <td>
<table class="bom_table">
  <thead>
  <tr>
      <th></th>
      <th>Item</th>
      <th>Material</th>
      <th>Quantity</th>
      <th>File</th>
  </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <img src="./src/figure/gripper/Base.png" style="width:100;">
      </td>
      <td>Base</td>
      <td>PLA</td>
      <td>1</td>
      <td>
        <a href="./src/stl/gripper/Base.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
    <tr>
      <td>
        <img src="./src/figure/gripper/Dynamixel_Mount.png" style="width:100;">
      </td>
      <td>Dynamixel Mount</td>
      <td>PLA</td>
      <td>2</td>
      <td>
        <a href="./src/stl/gripper/Dynamixel_Mount.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
    <tr>
      <td>
        <img src="./src/figure/gripper/Finger_Link.png" style="width:100;">
      </td>
      <td>Finger Link</td>
      <td>PLA</td>
      <td>2</td>
      <td>
        <a href="./src/stl/gripper/Finger_Link.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
    <tr>
      <td>
        <img src="./src/figure/gripper/Upper_Link.png" style="width:100;">
      </td>
      <td>Upper Link</td>
      <td>PLA</td>
      <td>2</td>
      <td>
        <a href="./src/stl/gripper/Upper_Link.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
    <tr>
      <td>
        <img src="./src/figure/gripper/Lower_Link_Half.png" style="width:100;">
      </td>
      <td>Lower Link Half</td>
      <td>PLA</td>
      <td>4</td>
      <td>
        <a href="./src/stl/gripper/Lower_Link_Half.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
  </tbody>
  <tbody class="table_bottom">
  <tr>
    <td>
      <img src="./src/figure/gripper/Finger_Tip.png" style="width:100;">
    </td>
    <td>Finger Tip</td>
    <td>TPU 95A</td>
    <td>2</td>
    <td>
      coming<br>
      soon
    </td>
  </tr>
  </tbody>
  <tbody class="table_bottom">
  <tr>
    <td>
      <img src="./src/figure/handle/Human_Handle.png" style="width:100;">
    </td>
    <td>Human Handle</td>
    <td>PLA</td>
    <td>1</td>
    <td>
      <a href="./src/stl/handle/Human_Handle.STL" download>
        <i class="fa-solid fa-download"></i>
      </a>
    </td>
  </tr>
  </tbody>
  <tbody class="table_bottom">
  <tr>
    <td>
      <img src="./src/figure/handle/Spot_Handle.png" style="width:100;">
    </td>
    <td>Spot Handle</td>
    <td>PLA</td>
    <td>1</td>
    <td>
      <a href="./src/stl/handle/Spot_Handle.STL" download>
        <i class="fa-solid fa-download"></i>
      </a>
    </td>
  </tr>
  </tbody>
  <tbody>
    <tr>
      <td>
        <img src="./src/figure/handle/Panda_Handle_1.png" style="width:100;">
      </td>
      <td>Panda Handle 1</td>
      <td>PLA</td>
      <td>1</td>
      <td>
        <a href="./src/stl/handle/Panda_Handle_1.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
    <tr>
      <td>
        <img src="./src/figure/handle/Panda_Handle_2.png" style="width:100;">
      </td>
      <td>Panda Handle 2</td>
      <td>PLA</td>
      <td>1</td>
      <td>
        <a href="./src/stl/handle/Panda_Handle_2.STL" download>
          <i class="fa-solid fa-download"></i>
        </a>
      </td>
    </tr>
  </tbody>
  <!-- Add more rows as needed -->
</table>

  </td>
  </tr>
</table>

<hr>

<table align=center width=800px>
  <tr>
    <td>
      <h2 id="assembly">Assembly Instruction</h2>
      Follow the video instructions below to assemble the shareable gripper components. Before assembly, use an appropriate press machine, such as 
      <a href="https://www.amazon.com/3DZWMAN-Vertical-Pressing-Machine-Printing/dp/B0BBSGG2S2/ref=sr_1_1_sspa?dib=eyJ2IjoiMSJ9.xwi5Z8Ac4o3C40kX2ATKJwKk8eZqPJHUw5pG6q7IVynCw7m4Z9II0Yw5ikXZk_0J-L52c3eaPi4GRs3z4IvAQMZc_wPrsfLugLdTQ4cVNZFyAKIVB0zg7ocLbHI-CUrX0vZlf7S26PNKQyEf-MfhjPZOZKIcOYGnmbMcErEFxARiBBNik6BFuaAgT36ClVihWKKAkYPFNyHZ2yHCe8kG__21kJIc-RTuV_TYTJRv-aU.vILq6JWPMIB46ILT9h3FteaFW0lgeJ6shOrOTYJAYQk&dib_tag=se&keywords=heat+insert+tool&qid=1731134766&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1
      ">
        <i class="fa-solid fa-link"></i>
      </a>, 
      to heat-set inserts into the <i>Base</i> part.
    </td>
  </tr>
  <tr>
    <td>
  <table border="0" cellspacing="10" cellpadding="0" align="center">
    <tbody>
      <tr>
        <td align="center" valign="middle">
          <video muted controls autoplay loop width="598">
            <source src="./src/video/assembly.mp4"  type="video/mp4">
          </video>
        </td>
      </tr>
    </tbody>
  </table>
    </td>
  </tr>
  <tr>
    <td>
      For use, you can assemble the sharabe gripper with the corresponding handles. Currently, we provide three types of handles: one for a human demonstrator, one for the Franka Emika <i>Panda</i>, and one for the Boston Dynamics <i>Spot</i>. The assembly instructions are shown in the following figures.
    </td>
  </tr>
  <tr>
    <td>
  <table border="0" cellspacing="10" cellpadding="0" align="center">
    <tbody>
      <tr>
        <td align="center" valign="middle">
          <a href="./src/figure/assembly/human.png"> 
            <img src="./src/figure/assembly/human.png" style="width:258;">
          </a>
        </td>
        <td align="center" valign="middle">
          <a href="./src/figure/assembly/panda.png"> 
            <img src="./src/figure/assembly/panda.png" style="width:258;">
          </a>
        </td>
        <td align="center" valign="middle">
          <a href="./src/figure/assembly/spot.png"> 
            <img src="./src/figure/assembly/spot.png" style="width:258;">
          </a>
        </td>
      </tr>
    </tbody>
  </table>
    </td>
  </tr>
</table>
<hr>
<table align=center width=800px>
  <tr>
    <td>
      <h2>Citation</h2>
    </td>
  </tr>
  <tr>
    <td>
    <!-- <left> -->
    <pre><code style="display:block; overflow-x: auto">
      @misc{seo2024legato,
        title={LEGATO: Cross-Embodiment Visual Imitation Using a Grasping Tool},
        author={Seo, Mingyo and Park, H. Andy and Yuan, Shenli and Zhu, Yuke and
          and Sentis, Luis},
        year={2024}
        eprint={2411.03682},
        archivePrefix={arXiv},
        primaryClass={cs.RO}
      }
    </code></pre>
    <!-- </left> -->
    </td>
  </tr>
</table>

<div class="page-width-background">
<div style="height: 4px;"></div>
<h2 align="center">Acknowledgement</h2>
<table align=center width=800px>
  <tr>
    <td> 
      <p align="justify" width="20%">
        This work was conducted during Mingyo Seo's internship at the AI Institute. We thank Rutav Shah and Minkyung Kim for providing feedback on this manuscript. We thank Dr. Osman Dogan Yirmibesoglu for designing the fin ray style compliant fingers and helping with hardware prototyping. We thank Mitchell Pryor and Fabian Parra for their support with the real Spot demonstration. We acknowledge the support of the AI Institute and the Office of Naval Research (N00014-22-1-2204).
      </p>
    </td>
  </tr>
</table>
<div style="height: 16px;"></div>
</div>
