**Title: Create web components for FHIR Resources**


![1589167270076](https://github.com/boluwalade/gsoc-fhir-webcomponents/assets/52458250/98d1cf4b-e2e9-4b12-83c0-0053657cf506)


**About me:**

I am a Health Informatics master's student in the department of BioHealth Informatics at Indiana University Purdue University Indianapolis. I am currently working on my thesis title 'building a user composable EHR system using FHIR web components". Over the last six months of working on my thesis, I have studied the FHIR healthcare exchange standards and its implementation in multiple works of literature. Additionally, I have also familiarized myself with the web components built in the previous GSOC projects and implemented some of the components in my work e.g. fhir-create-patient components. I have also studied and created some FHIR web components based using the polymer 3 library. By doing this, I have developed my JavaScript, HTML, CSS, Web Components and REST technical skills which will be useful in this project.

**Motivation:**

As a master's student in Health Informatics, I understand the challenges and barriers to establishing interoperability in the Electronic Health Record System and the solutions provided by the FHIR standard. This project presents me with an opportunity to contribute significantly to the development of an EHR system that supports FHIR Standards thereby promoting interoperability of healthcare data. The components built could also be used in other EHR systems. The potential benefits of this project in healthcare is a motivating factor for me.

**AIM**

- The aim of this project is to create web components for the LibreHealth EHR based on FHIR resources using the polymer library.
- Incorporate built components into the lh-toolkit app

**DESCRIPTION**

The FHIR resources were developed by the HL7 standard development organization as a healthcare data exchange standard based on Rest API technology. This enables data exchange with the use of HTTP endpoints. According to the FHIR documentation, a FHIR resource contains an URL identity, information about the type of resource, a set of structured data items as defined by the type of resource and an identified version that changes based on changes in the resource content.

Polymer is an open-source library for creating and using custom elements. It abstracts some repetitive boilerplate code thus allowing web developers to focus on the application logic. Polymer also provides polyfills that ensure that web components work on different browsers that are fully yet to support web components hence there are no discrepancies in usage. Polymer also adds data binding features that make it easier to order data flow within components and web applications. The FHIR components are built using the polymer library.

To ensure scalability and reusability, the components are built based on the resource contents of the FHIR resources. These components will be of use to EHR developers to upgrade to a common data model. An example is the Encounter Resource. A snippet of the resource content from the FHIR resource page is shown in figure 1 below. A mockup for the web component for this resource is shown in figure 2.

Figure 1: Encounter Resource content
<img width="452" alt="Pictur1" src="https://github.com/boluwalade/gsoc-fhir-webcomponents/assets/52458250/1f34f077-f8f8-4249-b32f-d79317d48928">



Figure 2:

<img width="452" alt="Pictur2png" src="https://github.com/boluwalade/gsoc-fhir-webcomponents/assets/52458250/f009f133-5fea-4b7f-b264-f281e037316c">

Figure 2 above has multiple reusable components such as the Encounter status, Encounter class, Encounter priority, Encounter type, etc. Mockups of some of the components are shown below


**DELIVERABLES** :

- Repository of various web components with their documentation
- An updated LibreHealth toolkit app with the FHIR backend

**PROJECT IMPLEMENTATION PLAN**

**1.**** Resources Understanding and Mockups creation**

Resources are broken down into smaller components based on their contents to enable ease of use. These components when assembled will represent an FHIR resource. Some mockups of these components are created using Balsamiq wireframes as shown in the figures above.

**2.**** Development and testing of components**

In previous year's projects, components for different resources have been created, they include allergy, appointment,location,organization, patient and practitioner. The resources are composed of subcomponents that form resource components when assembled. Some UI components such as the fhir-login,fhir-navbar,fhir-search and fhir-searchbox have also been created. I will create components for the Observation, Medication, MedicationRequest and MedicationStatement resources. They will be broken down into subcomponents for ease of development. These components are mostly level 3 maturity level except the Observation resource which is a normative content.

Based on the mockups created earlier, the components for the resources are developed using the polymer 3 library. These components are created based on a similar structure and form of previous year's projects such as the use of the material web components and vaadin web components (Links to the documentation for the components are listed in the appendix). This ensures consistency in design and documentation. Adequate documentation on the usage of each component is found in the README.md file in the respective GitHub repositories. The process of developing each component is tracked using Github.

Also, Unit testing of these components is done using the Web Component Tester by Polymer. Instructions on the usage of the Web Component Tester is available at[https://github.com/Polymer/tools/tree/master/packages/web-component-tester](https://github.com/Polymer/tools/tree/master/packages/web-component-tester).

The created and tested components will be subsequently pushed to the LibreHealth web components repository. An example component that I created can be accessed at [https://github.com/boluabraham/fhir-observation-status](https://github.com/boluabraham/fhir-observation-status)

**3.**** Assembly the component into the LH-toolkit-App**

The created components are incorporated into the lh-toolkit-app.

A short video showing some modifications I made locally to the app can be accessed at [https://youtu.be/TU8-8Lc-I7A](https://youtu.be/TU8-8Lc-I7A). These modifications are intended to comply with the current layout of the lh-toolkit app. An alternate layout could also be made such as depicted in figure 3 and 4 below:

Figure 3
<img width="409" alt="Pictur3" src="https://github.com/boluwalade/gsoc-fhir-webcomponents/assets/52458250/089b30e7-8ddf-4395-8f66-f2b13abbfeae">
Figure 4

<img width="408" alt="Pictur4" src="https://github.com/boluwalade/gsoc-fhir-webcomponents/assets/52458250/e9e82b8c-f3ac-46f2-9296-307298c27f44">


Figure 3 shows the use of a sidebar navigation content where each of the tabs links to a different page. Figure 4 shows an example of the patient page that can be accessed by clicking on the "Patient" tab in figure 3. In the "Patient" page in figure 4, there are two tab bars titled "Create Patient" and "Search Patient" respectively. These tab bars contain different pages containing the appropriate FHIR resource components

**Component Assembly**

I would update the components list of the LH-toolkit app by incorporating the newly created components. Documentations of the polymer PWA template is available at [https://github.com/Polymer/pwa-starter-kit/blob/master/README.md](https://github.com/Polymer/pwa-starter-kit/blob/master/README.md). Here an appropriate template is selected and the elements are copied to the based on the 'src/component'. A uniform theme for the application is obtained by updating the shared-styles.js file in the 'src/component' folder. This serves as a source for the styling of the components. This style is imported into the web page containing all the new elements, thus conforming with the UI's theme.

**TIMELINE:**

I am able to work an average of 40 hours weekly. The proposed timeline is described below;

**Before May 4:**

Familiarize myself with the FHIR Resources.

- Review and Familiarize with the project's submission from the previous years (2018 and 2019)
- Study more on the polymer library and build some web components.

**May 4 – May 31:**

- Community Bonding with the LibreHealth community and Mentor
- Divide the proposed resources into subcomponents
- Understanding of Resources and Creation of Mockups for components

**June 1 – August 31: Coding Period**

- June 1 — July 10 (At least 4 components per week)
  - Building of the components
  - Mentor evaluation (July 1)
- June 13 – July 24
  - Unit testing of the built components
- July 27 -July 31
  - Review documentation for each component
  - Mentor evaluation (July 31)
- August 3 – August 14
  - Building of the LH-toolkit app from the components
- August 17- August 21
  - Refine tests and documentation for the whole project and integrate into the lh-toolkit repository
- August 24 -28
  - Buffer week to in case of unforeseen delays
- August 28
  - Project submission and final mentor evaluation submission

**APPENDIX**

Material components:[https://material.io/components/](https://material.io/components/)

Vaadin components:[https://vaadin.com/components](https://vaadin.com/components)
