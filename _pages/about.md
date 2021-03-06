---
permalink: /
title: "Investigating the effects of turbulence modulation in particle-laden gas turbine engines"
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Introduction
======
Dispersed multiphase flows are ubiquitous in both nature and engineering with common examples including atmospheric dispersal of pollutants, liquid sprays in engines, and sedimentation of sand particles in river beds. In aviation, a critical example of dispersed multiphase flow involves the ingestion of solid particulates in fixed-wing and rotary-wing engines. Guffanti et al. report on over 79 incidents in which aircraft encounters with volcanic ash clouds led to severe engine damage. Similarly, there have been many reported rotorcraft incidents caused by brownout, a phenomenon in which the rotor downwash causes a cloud of sand to engulf the helicopter, such as the fatal V-22 Osprey crash landing in May 2015. In many of these incidents, sand or volcanic ash ingestion in the gas turbine engine lead to power-loss or complete engine failure.

There are three main damage mechanisms that can lead to failure for a modern gas turbine powered aircraft: erosion, clogging, and deposition. Volcanic ash or sand entering a gas turbine engine at high velocities can erode the compressor and turbine blades, negatively impacting the aerodynamic efficiency. These solid particles can also clog cooling channels and fuel nozzles, leading to overheating and poor combustion. If the turbine inlet temperature is very high and the particles contain glassy constituents, the particles can melt and deposit on the turbine blades. This deposition can attack the protective thermal barrier coating, increasing thermal stresses on the blades which in turn lead to blade failure. Premature failure of a gas turbine engines due to solid particle ingestion is not only costly but dangerous, leading many researchers to focus their efforts on these phenomena.

Substantial progress has been made to understand the effects of erosion, clogging, and deposition within a gas turbine engine; however, there is still more work required to characterize the underlying physics behind these mechanisms. One aspect of this characterization involves studying the effects that the ingested particles have on the overall flow field. Gas turbines operate at high Reynolds numbers and transonic Mach numbers causing the internal flow to be both turbulent and unsteady. The addition of ingested particles subject to such conditions only adds to the complexity of the flow. Ingested sand, salt, and volcanic ash are typically comprised of CMAS (calcium-magnesium-alumino-silicate) which are susceptible to phase change when exposed to high temperatures such as the conditions in the combustor\cite{Grant2007}. As sand/salt/volcanic ash exits the combustor, it is typically in a semi-molten or molten state, making it receptive to deposition onto the turbine blades. While many research efforts have been made to understand the deposition process for semi-molten and molten phase particles, there is still a need to understand the transport characteristics of these particles prior to deposition. Specifically, studies have shown that particle-laden flows display a variety of interesting phenomena that significantly impact the turbulent flow field and consequently the deposition rate. These phenomena include preferential accumulation of dispersed particles, variations to interphase coupling, turbulence modulation, and turbophoresis. 

Proposed Research Methodology
======

Preliminary Findings
------
A preliminary investigation by Jain et al. used Large Eddy Simulation (LES) with Lagrangian particle tracking to examine the particle deposition characteristics of molten sand on a turbine blade as a function of Stokes number. This study showed that particles with small Stokes numbers (St << 1) behave like tracer particles, following the streamlines and avoiding the blade surface. However as the Stokes number became significantly large (St >> 1), the particles inertia led to ballistic impingement and deposition on the blade surface. In addition, the authors note that the large Stokes number regime led to significant modulation of the flow field turbulence. As such, the results from this study suggest that in order to adequately characterize molten particle deposition, the entire range of spatial and temporal scales of turbulence surrounding the particles must be realized. 

The objective of this proposed research study is to numerically investigate the impact that phase change has on turbulence modulation for sand particles ingested in the hot section of a gas turbine jet engine in order to characterize molten sand transport prior to deposition. A detailed Direct Numerical Simulation (DNS) with Lagrangian particle tracking will be used in order to establish a complete description of this environment with the expectation that novel insights into the underlying physics behind molten particle turbulence modulation will be established. The following section outlines the proposed research plan which subdivides the project into three distinct phases.

Research Plan
------

**Phase I**
DNS offers a way to obtain a complete description of a turbulent flow by numerically solving the unsteady, 3-D Navier Stokes equations down to the Kolmogorov length scale. With the recent increase in computational power, DNS is now capable of simulating complex instantaneous flow fields that are comparable, providing a much higher spatio-temporal resolution, than what is currently possible in experimental methods. In order to study a moderately dense particle-laden flow, as seen with sand ingestion in gas turbine engines, the DNS must be coupled with a Lagrangian, point-particle method (PP-DNS). The PP-DNS computational solver, Athena-RFX, has been selected for the proposed research study. Athena-RFX is a massively parallel, fully compressible, high order, dimensionally unsplit, reactive flow code which is an extension of the magnetohydrodynamic code Athena. 

Phase I of this project will give special attention to preparing and running Athena-RFX test cases at the DoD Supercomputing Resource Center (DRSC). These test cases will begin simply with single-phase DNS and incrementally evolve into DNS with Lagrangian massive particle tracking. This will ensure that both the DNS and Lagrangian point-particle methods are understood and behave as expected. Concurrently, Athena-RFX source code will be examined in order to promote developmental processes for Phase II.


**Phase II**
Before studying the effects that molten sand particles have on turbulence modulation, modifications to Athena-RFX must be made. The Lagrangian point-particle method in Athena-RFX is currently limited to modeling massive solid and liquid particles separately without accounting for solid-to-liquid phase change. As such, modifications to the source code will need to be implemented in order to accurately model the solid-to-liquid phase change of sand particles.  

Phase II of this project will focus on the determination and implementation of the most suitable phase change model for this application. Heat transfer between the carrier-phase and dispersed-phase is the main mechanism driving the phase change. In Athena-RFX, the particle equations are completely coupled with the flow equations and exchange mass, momentum, and energy. There is also a model for particle heat transfer already included in Athena-RFX. The main focus of Phase II will be to determine the best way to incorporate the phase transition from solid to liquid. Once the method has been implemented, rigorous testing will ensue to assure the phase change modelling is correct.


**Phase III**
The first half of Phase III can be performed concurrently with Phase II. This includes preliminary studies on inert particles in wall-bounded turbulent channels. Testing with solid inert particles will be performed while the development of the phase change model is still underway. A preliminary case will be done to replicate the results of the study performed by Fong et al.. This study looks at the velocity and spatial distributions of inert glass beads in a turbulent channel for various particle volume-fractions. This study is a good lead in to studying the effects of turbulence modulation. Upon successful implementation of the phase change model in Phase II, the main investigation of phase change influence on turbulence modulation will begin. Simulations of sand particles in gas turbine conditions will be performed and resulting analysis will follow.

Expected Results
======

The primary outcome of this proposed research is the development of a multiphase PP-DNS solver which can study the impact of molten sand on turbulence modulation in wall-bounded turbulent flows. Upon the successful implementation, the solver will be used to study various Stokes numbers and particle mass loadings in order to develop criteria for particle deposition near a wall. Thorough examination of these simulation will be used to obtain a deeper understanding into the underlying physics that lead to turbulence modulation in particle-laden gas turbine flows as a function of solid-to-liquid phase change. In addition, the results will be used to improve particle transport models that govern the material deposition process in order to assist in the development of CMAS-attack mitigation strategies. 
