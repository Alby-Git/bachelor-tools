<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://galaxyproject.org/">
    <img src="images/galaxy_project_logo.png" alt="Logo" width="250" height="80">
  </a>

<h2 align="center">Bachelor's Project </h2>
  <p align="center">
    Port, improve, and benchmark read-based MGnify analysis pipeline for microbiome data using the Galaxy framework
  <h4 align = "center"> by Albert Ratschinki </h4>
    <br />
    <a href="https://github.com/Alby-Git/bachelor-tools"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/Alby-Git/bachelor-tools/tree/main/tools/mOTUs"><strong> mOTUs </strong></a> 
    ·
    <a href="https://github.com/Alby-Git/bachelor-tools/tree/main/tools/seqprep"><strong> SeqPrep </strong></a> 
    <br />
    <br />
    <a href="https://github.com/github_username/repo_name">SepPrep IUC</a>
    ·
    <a href="https://github.com/github_username/repo_name">mOTUs galaxy tools</a>
    ·
    <a href="https://github.com/Alby-Git/bachelor-tools/issues">Report Bug</a>
    ·
    <a href="https://github.com/Alby-Git/bachelor-tools/issues">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<!--[![Product Name Screen Shot][product-screenshot]](https://galaxyproject.org/images/galaxy-logos/galaxy_project_logo.png)
-->

From October 16th to January 16th, I embarked on a bachelor's project as part of my Bachelor's degree at the Professorship for Bioinformatics. Supervised by [Paul Zierep](https://github.com/paulzierep), my task was to port, improve, and benchmark the read-based MGnify analysis pipeline for microbiome data using the Galaxy framework.

### Project Overview

Microbiome data analysis is a complex field, necessitating advanced computational tools and methodologies. My project centered on the [MGnify V5 Raw reads Pipeline](https://www.ebi.ac.uk/metagenomics/pipelines/5#raw), a well-regarded pipeline in microbiome data analysis.

A significant part of my project involved wrapping the tools [SeqPrep](https://github.com/jstjohn/SeqPrep) and [mOTUs3](https://github.com/motu-tool/mOTUs) (an updated version compared to mOTUs2 as illustrated in the image) for integration into the [Galaxy platform](https://galaxyproject.org/). This integration was crucial as it allows the full workflow of the MGnify V5 pipeline to be executed within Galaxy, making it accessible for a broader range of researchers and facilitating ease of use.

<br>
<div align="center" style="width: 80%; margin: auto;">
  <figure>
    <a href="https://www.ebi.ac.uk/metagenomics/pipelines/5#raw">
      <img src="images/mgnifyV5.png" alt="MGnify Version 5 Logo" style="width: 100%; height: auto; border: 5px solid #7b2cbf;">
    </a>
    <figcaption>An illustration of the MGnify V5 pipeline</figcaption>
  </figure>
</div>



<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started
Follow these steps to use SeqPrep on the Galaxy platform and prepare for the upcoming integration of mOTUs.

### Preparations

Before starting, ensure you have created an account on [Galaxy](https://usegalaxy.eu/). Galaxy offers a web-based platform with a wide array of bioinformatics tools for research.

### Using SeqPrep in Galaxy

SeqPrep is going to be integrated into Galaxy and can be used for preprocessing microbiome sequencing data. Here's how to use it:

1. **Create a Galaxy Account:**
  - Visit [usegalaxy.eu](https://usegalaxy.eu/) and create an account if you don’t already have one.

2. **Find the SeqPrep Tool:**
  - Once logged in to Galaxy, search for "SeqPrep" in the tool search bar.

3. **Upload Data:**
  - Upload your microbiome sequencing data to Galaxy.

4. **Configure SeqPrep:**
  - Select SeqPrep from the list of tools and configure it according to your specific requirements for your data.

5. **Run SeqPrep:**
  - Execute the tool and wait for the results. SeqPrep will process your data

appropriately, preparing it for further analysis.

### Future Integration of mOTUs

Currently, mOTUs is not yet directly integrated into Galaxy, but work is underway to make this tool available soon. Once mOTUs is integrated into Galaxy, it will enable efficient and user-friendly metagenomic analyses. Keep an eye on updates in our repository to stay informed about the integration of mOTUs.


<!-- USAGE  -->
## Usage

The tools and methodologies developed in this project can be applied in various ways to facilitate and enhance microbiome data analysis. Below are some examples of how these tools can be utilized within the Galaxy framework:

### Example Use Cases:

1. **Microbiome Data Preprocessing with SeqPrep:**
   - Utilize SeqPrep for the preprocessing of microbiome sequencing data. This includes steps like merging paired-end reads and quality filtering.
   - Example Workflow:    
      - After uploading your paired-end sequencing data to Galaxy, select SeqPrep from the tool menu.
      - Configure the tool parameters: specify the input files for forward and reverse reads, and set the merging and quality filtering parameters according to your experiment's requirements.
      - Execute the tool to process the data. The output will be a single, merged file of high-quality reads, ready for further analysis.

2. **Metagenomic Analysis with mOTUs:**
   - Deploy mOTUs for metagenomic profiling. This tool helps in identifying and quantifying microbial taxa in the sample data.
   - Example Workflow: 
      - Start with high-quality, preprocessed reads (e.g., output from SeqPrep).
      - Select mOTUs from the Galaxy tool menu.
      - Input your reads into mOTUs. You may need to specify certain      parameters, like the type of analysis (e.g., species-level profiling) or other advanced settings based on your study.
      Run the tool. mOTUs will output a detailed profile of the microbial community present in your sample.
      - This output can be visualized directly in Galaxy using available visualization tools or exported for further analysis.

### Integrating Tools in Galaxy:

- **Galaxy Environment:** 
  - [Galaxy](https://galaxyproject.org/) is an open, web-based platform for computational biomedical research. It allows users to reproduce and share analyses.
  - Within Galaxy, tools like SeqPrep and mOTUs can be integrated to streamline and simplify the microbiome data analysis pipeline.

### Additional Resources and Documentation:

- For detailed instructions, use cases, and tutorials on how to use these tools in Galaxy, please refer to the [Galaxy Training Network](https://training.galaxyproject.org/training-material/).


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

**Planemo**
- [x] **Install and Configure Planemo**
  - Setup Planemo environment on the system.
- [x] **Planemo Tutorial**
  - Complete introductory tutorials for understanding Planemo's functionalities.
- [x] **Planemo Documentation**
  - Extensive reading of the [Planemo Documentation](https://planemo.readthedocs.io/en/latest/index.html) to deepen understanding.

**SeqPrep**
- [x] **Understanding SeqPrep**
  - Research [SeqPrep](https://github.com/jstjohn/SeqPrep) tool and its mechanisms.
- [x] **Blueprint for SeqPrep**
  - Develop a plan for wrapping SeqPrep using Planemo.
- [x] **Implement SeqPrep in Galaxy**
  - Successfully wrap SeqPrep and demonstrate its functionality on Galaxy.
- [x] **Contribute to IUC**
  - Prepare and submit a pull-request to integrate SeqPrep into the IUC main branch. (Here)[https://github.com/galaxyproject/tools-iuc/pull/5719]

**mOTUs**
- [x] **Explore mOTUs**
  - Learn about the mOTUs tool and its applications.
- [x] **Plan mOTUs Integration**
  - Design a strategy for incorporating mOTUs into Galaxy.
- [ ] **Galaxy Implementation**
  - Execute the integration of mOTUs into the Galaxy platform.
- [ ] **Testing and Validation**
  - Ensure mOTUs works seamlessly within Galaxy; perform tests.
- [ ] **Contribute to bgruening-galaxytools
  - Prepare and submit a pull-request to integrate mOTUs into the galaxytools branch from bgruening main branch.
  
- [ ] **Understand Data Manager Requirements**
  - Study the specific needs for a data manager for mOTUs.
- [ ] **Development Plan**
  - Draft a comprehensive plan for developing the mOTUs data manager.
- [ ] **Implementation**
  - Develop and integrate the data manager into the Galaxy ecosystem.
- [ ] **Optimization and Review**
  - Optimize for performance and user-friendliness; prepare for peer review.

For a full list of proposed features and known issues, see the [open issues](https://github.com/Alby-Git/bachelor-tools/issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Albert Ratschinki -  albert.ratschinki@email.com

Project Link: [https://github.com/Alby-Git/bachelor-tools](https://github.com/Alby-Git/bachelor-tools)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Planemo 101

### Installation

1. **Install Planemo:**

   - For more information, visit the [Planemo documentation](https://planemo.readthedocs.io/en/latest/).

### Test

1. **Running Tests:**

   - To test your Galaxy tools, use the following Planemo command:
     ```sh
     planemo test --galaxy_root /path/to/galaxy_root my_tool.xml
     ```

### Serve

1. **Running a Local Galaxy Server:**

   - To serve your tools in a local Galaxy instance, use this command:

     ```sh
     planemo serve --galaxy_root /path/to/galaxy_root my_tool.xml
     ```

   - This will start a local Galaxy server where you can test your tools in a real Galaxy environment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Acknowledgments

Special thanks to:

* **Paul Zierep:** For his mentorship and expertise in guiding the development and implementation of the project, particularly in the areas of bioinformatics and data analysis.
* **Rand:** For the significant assistance with Planemo and SeqPrep, facilitating key aspects of the project's development.
* **Galaxy Project Team:** For providing an excellent platform for bioinforma
tics research.
* **SeqPrep and mOTUs Developers:** For their contributions to microbiome data analysis tools.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

