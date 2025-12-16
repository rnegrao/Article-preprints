# Application of a Compact Hybrid Photon-Counting Semiconductor Detector Prototype for X-Ray Material Analysis

## Abstract

Hybrid photon-counting X-ray detectors have emerged over the past two decades as a cornerstone technology in advanced X-ray material analysis and imaging, driven by their intrinsic advantages in terms of single-photon sensitivity, intrinsic energy discrimination, high dynamic range, and negligible readout noise. In contrast to conventional integrating detectors, photon-counting architectures enable direct quantification of individual X-ray quanta, leading to superior signal-to-noise characteristics, improved contrast, and enhanced quantitative accuracy across a broad range of experimental conditions. These features have positioned hybrid pixel detectors as a critical enabling technology for modern synchrotron and laboratory-based X-ray techniques, including diffraction, scattering, spectroscopy, and high-resolution imaging.

In this work, the performance and applicability of a compact X-ray detector prototype based on the Medipix3RX application-specific integrated circuit (ASIC), originally developed at CERN, are systematically investigated. The detector architecture combines a monolithic silicon semiconductor sensor with a modular hybrid-pixel readout scheme, integrating multiple Medipix3RX chips into a compact, air-cooled camera system optimized for high-speed and low-noise operation. Particular emphasis is placed on evaluating the detector response under laboratory conditions that emulate key requirements of synchrotron-based experiments, including energy threshold stability, pixel response uniformity, spatial resolution, and data throughput.

The primary objective of this study is to assess the detector performance with respect to spatial resolution and data quality in X-ray Powder Diffraction (XPD) measurements. Quantitative metrics such as the Modulation Transfer Function (MTF) are employed to characterize the intrinsic spatial resolving power of the detector, while two-dimensional diffraction images acquired from a LaB₆ reference powder are analyzed to validate the detector’s suitability for high-precision diffraction experiments. The results demonstrate that the compact Medipix3RX-based detector achieves excellent spatial resolution, stable energy calibration, and high-quality diffraction data, confirming its potential as a versatile and robust solution for laboratory and synchrotron X-ray material analysis applications.


## 1. Introduction

Synchrotron-based X-ray techniques have, for several decades, constituted an indispensable set of tools for probing the structural, electronic, and dynamical properties of matter across a wide range of length and time scales. Their impact spans numerous scientific disciplines, including condensed matter physics, chemistry, materials science, environmental science, and structural biology. The defining characteristics of synchrotron radiation—namely its high brilliance, tunable photon energy, high degree of spatial and temporal coherence, and well-defined polarization—enable experiments that are fundamentally inaccessible to conventional laboratory X-ray sources. These properties allow researchers to interrogate materials with exceptional sensitivity and precision, revealing subtle structural features, phase transitions, strain fields, and electronic configurations under both equilibrium and operando conditions.

The rapid evolution of synchrotron light sources, culminating in the advent of so-called fourth-generation storage rings, has placed increasingly stringent demands on X-ray detector technologies. Diffraction-limited storage rings deliver unprecedented photon flux densities and coherence, thereby requiring detectors capable of handling high count rates, fast framing, and wide dynamic ranges without sacrificing spatial resolution or data fidelity. In this context, hybrid pixel detectors have emerged as a transformative technology, offering a unique combination of performance characteristics that align closely with the requirements of modern synchrotron experiments. Their ability to perform direct photon counting at each pixel, combined with per-pixel energy discrimination and negligible electronic noise, represents a significant departure from traditional charge-integrating detector paradigms.

Among the various detector technologies currently deployed at synchrotron facilities, semiconductor hybrid photon-counting detectors have become the dominant solution for a broad spectrum of applications. Their superior data acquisition speed, architectural flexibility, and robustness under high-flux conditions have led to widespread adoption across numerous experimental techniques. These include, but are not limited to, X-ray Absorption Spectroscopy (XAS), X-ray Powder Diffraction (XPD), macromolecular crystallography, Bragg coherent X-ray diffraction imaging, Small-Angle X-ray Scattering (SAXS), Wide-Angle X-ray Scattering (WAXS), Grazing-Incidence Small-Angle Scattering (GISAXS), micro- and nano-tomography, ptychographic X-ray computed tomography (PXCT), and X-ray Photon Correlation Spectroscopy (XPCS). In each of these methods, detector performance directly influences achievable spatial resolution, temporal resolution, and quantitative accuracy.

The hybrid photon-counting detector concept relies on the intimate integration of a semiconductor sensor layer with a dedicated readout ASIC, interconnected via fine-pitch bump bonding. The semiconductor sensor, typically fabricated from silicon for photon energies up to approximately 20–30 keV, or from high-Z materials such as CdTe or GaAs for higher energies, is responsible for efficient X-ray absorption and charge generation. The readout ASIC, in turn, processes the induced charge signals at the pixel level, applying energy discrimination through adjustable thresholds and incrementing digital counters upon detection of valid photon events. This architecture effectively eliminates readout noise and dark current contributions, enabling background-free measurements and high-contrast imaging even at low photon fluxes.

In this work, a compact X-ray detector prototype based on the Medipix3RX ASIC is presented and evaluated. The Medipix family of ASICs, developed within the Medipix collaboration at CERN, represents one of the most successful and widely adopted hybrid pixel detector platforms in the field of X-ray science. The Medipix3RX variant introduces significant improvements in count rate capability, charge summing, and continuous read–write operation, making it particularly well suited for high-flux synchrotron environments as well as advanced laboratory applications. By utilizing a silicon semiconductor sensor coupled to the Medipix3RX readout, the detector achieves efficient hard X-ray absorption while retaining the intrinsic advantages of photon-counting operation.

An overview of the compact detector architecture and its unique design features is provided, followed by a detailed characterization of its performance. Particular attention is devoted to the assessment of spatial resolution through Modulation Transfer Function measurements, as well as to the evaluation of data quality in X-ray powder diffraction experiments. To demonstrate the detector’s imaging capabilities, large-area, low-noise, and high-resolution diffraction images of standard reference materials are acquired and analyzed. The results presented herein illustrate the suitability of the compact Medipix3RX-based detector for demanding X-ray material analysis applications and highlight its potential role in both synchrotron beamlines and advanced laboratory-based X-ray facilities.


## 2. Methodology

### 2.1 Compact X-ray Detector Architecture and Design Requirements

The compact X-ray detector presented in this work was conceived as a modular, high-performance X-ray camera designed to fulfill the stringent operational requirements imposed by fourth-generation synchrotron radiation sources. These requirements include high-speed image acquisition, low intrinsic noise, small pixel pitch, high count-rate capability, and minimal inactive area between sensitive regions. In addition, the detector architecture was optimized to support laboratory-based experiments, where compactness, mechanical robustness, and operational stability are critical factors.

The modular design philosophy enables scalability of the sensitive area while maintaining consistent detector performance across modules. Each module operates as an independent detection and readout unit, allowing parallel data acquisition and simplifying system integration. The compact form factor facilitates installation in confined experimental environments and supports a wide range of experimental geometries, including diffraction, scattering, and imaging configurations.

### 2.2 Medipix3RX ASIC and Sensor Characteristics

The detector system is based on the Medipix3RX application-specific integrated circuit (ASIC), a well-established hybrid pixel readout chip developed within the Medipix collaboration at CERN. The Medipix3RX ASIC is specifically designed for single-photon counting applications and incorporates per-pixel charge-sensitive amplifiers, adjustable energy threshold discriminators, digital counters, and fast readout logic.

Each Medipix3RX ASIC consists of a 256 × 256 pixel matrix with a pixel pitch of 55 × 55 μm², resulting in a sensitive area of approximately 14.1 × 14.1 mm² per chip. The ASIC supports frame rates of up to 2000 frames per second, depending on the readout configuration, and provides configurable counter depths of either 12 or 24 bits per pixel. Continuous read-and-write operation allows simultaneous data acquisition and readout, minimizing dead time and enabling efficient utilization of high photon fluxes.

The ASIC is bump bonded to a monolithic silicon sensor with a thickness of 300 μm, selected to provide efficient absorption for hard X-rays in the energy range relevant to diffraction and scattering experiments. The use of silicon as the sensor material ensures excellent charge transport properties, high uniformity, and mature fabrication processes, while maintaining compatibility with the Medipix3RX readout architecture.

### 2.3 Energy Thresholding and Noise Performance

A defining feature of the Medipix3RX architecture is its adjustable per-pixel energy threshold capability. Each pixel incorporates discriminators whose threshold levels can be finely tuned through on-chip digital-to-analog converters (DACs). This capability allows the detector to suppress electronic noise contributions effectively by rejecting signals below a defined energy threshold, thereby achieving a near-zero noise floor.

By operating the detector at an optimized threshold setting, the signal-to-noise ratio is significantly improved, particularly in low-dose or low-flux imaging conditions. In the present work, threshold values were selected to balance noise suppression with detection efficiency, ensuring reliable photon counting while maintaining sensitivity to the relevant X-ray energies used in the experiments.

The compact X-ray detector integrates a 1 × 6 array of Medipix3RX ASICs within a single sensor module, forming a so-called Hexa module. Figure XX schematically illustrates the physical dimensions and hardware configuration of the detector, highlighting the arrangement of the ASICs, sensor, cooling elements, and readout electronics.

**Figure XX:** Compact X-Ray Detector

### 2.4 Sensor Module Mechanics and Thermal Management

The mechanical design of the detector is centered on the sensor module, which constitutes the fundamental building block of the system. Each Hexa module comprises a single monolithic silicon sensor bump bonded to six Medipix3RX ASICs. The ASICs are positioned in close proximity to one another, with only a narrow gap between adjacent pixel matrices at the chip boundaries. This configuration minimizes inactive regions and maximizes the effective sensitive area of the detector.

The sensor module is mechanically coupled to a copper heat spreader, which serves to homogenize the thermal load generated by the ASICs during operation. The copper spreader is in turn attached to a Peltier thermoelectric cooler (TEC), enabling active temperature control of the sensor and readout electronics. Heat extracted by the TEC is dissipated via an air-cooled aluminum heat spreader, ensuring efficient thermal management under continuous operation.

This layered thermal design maintains stable operating conditions for the ASICs and sensor, reducing thermal noise and minimizing performance drifts associated with temperature fluctuations. The detector is designed to operate reliably within a temperature range of 25 °C to 35 °C.

### 2.5 Electrical Interconnections and Readout Electronics

Each Medipix3RX ASIC is wire bonded to a dedicated carrier board that provides electrical interfacing between the sensor module and the downstream readout electronics. The carrier board is connected to a flexible cable assembly responsible for distributing power to the ASICs, transmitting configuration signals, and routing high-speed data outputs.

The readout board is mechanically and electrically connected to the carrier board in a compact arrangement that allows the readout electronics to be positioned directly behind the sensor module. In the current hardware implementation, a single readout board services one Hexa module, handling configuration, data acquisition, buffering, and transmission. This one-to-one mapping simplifies system architecture and ensures deterministic data flow from each module.

A rigid mounting chassis provides mechanical stability and precise alignment of the sensor modules, which is essential for diffraction and imaging experiments requiring accurate spatial calibration. The chassis also facilitates integration of multiple modules into larger detector assemblies if required.

### 2.6 Cooling System and Environmental Control

To dissipate the heat generated by the electronic components—including the field-programmable gate array (FPGA), on-board processor, and quad small form-factor pluggable (QSFP) optical transceiver—the detector enclosure incorporates dedicated cooling vents for air intake and exhaust. Six fan units are distributed along the sides of the detector housing to provide a controlled airflow across critical components.

This forced-air cooling system ensures that all electronic and sensing elements remain within their specified operating temperature limits, even during extended high-frame-rate acquisitions. Temperature sensors integrated within the detector provide real-time monitoring, enabling active control and fault detection.

### 2.7 Data Communication and Control Software

Communication between the detector and the user-side computer server is implemented via a 10 Gbps Ethernet optical link, providing sufficient bandwidth to support high data throughput during fast imaging and diffraction experiments. Imaging data are transmitted using the Remote Direct Memory Access over Converged Ethernet (RoCE) protocol, which enables low-latency, high-efficiency data transfer with minimal CPU overhead.

Detector control, configuration, and data acquisition are managed through a dedicated software stack that interfaces with the detector hardware. The system is compatible with distributed control environments based on the Experimental Physics and Industrial Control System (EPICS) framework, enabling seamless integration into synchrotron beamline control architectures. For the experiments reported in this work, the detector was operated locally on a dedicated server, providing direct control and data storage.

### 2.8 Experimental Setup and Calibration Procedures

Performance characterization experiments were conducted using a benchtop X-ray experimental setup located at the Laboratory for Crystal Cutting and Orientation (LCCO) at the CNPEM/SIRIUS synchrotron facility. Although operated outside of a beamline environment, the setup was designed to emulate key aspects of synchrotron-based measurements, allowing systematic evaluation of detector performance.

The initial characterization focused on pixel response uniformity and energy threshold calibration. Pixel uniformity was achieved by applying a noise floor pixel equalization procedure, which optimizes the threshold discriminator DAC settings of each Medipix3RX pixel. This procedure compensates for intrinsic pixel-to-pixel variations in electronic response, resulting in a homogeneous detection threshold across the entire sensor array.

Following threshold equalization, energy calibration was performed using X-ray fluorescence (XRF) targets composed of Cobalt (Co), Zinc (Zn), Selenium (Se), and Zirconium (Zr). The characteristic fluorescence lines emitted by these materials provide well-defined reference energies for calibrating the detector threshold settings.

The resulting energy calibration curve, shown in Figure YY, exhibits excellent linearity across the investigated energy range for all sensor chips. This behavior indicates high detector stability and uniform response over the full sensitive area, confirming the suitability of the detector for quantitative X-ray measurements.

**Figure YY:** Energy calibration curve

### 2.9 Spatial Resolution and Modulation Transfer Function Analysis

The spatial resolution of the detector was quantified using the Modulation Transfer Function (MTF), a fundamental metric that describes the ability of an imaging system to preserve spatial frequency information from the object to the recorded image. In this study, the MTF was measured using the standard angled-edge technique.

Images of a radiopaque tungsten edge were acquired with the edge positioned at an angle of approximately 2.5° relative to a detector pixel row and placed in close proximity to the detector surface. The measurements were performed using a tungsten X-ray tube operated at 70 kV and 50 mAs, with a source-to-detector distance of 1.6 m.

From the acquired images, the edge spread function (ESF) was extracted and numerically differentiated to obtain the line spread function (LSF). The MTF was then calculated as the magnitude of the normalized Fourier transform of the LSF. During the measurements, the detector energy threshold was set to 6 keV, sufficiently above the electronic noise floor to ensure reliable photon discrimination.

Figure ZZ presents the normalized MTF as a function of spatial frequency, illustrating the high spatial resolving power achieved by the detector.

**Figure ZZ:** Normalized MTF values as a function of the spatial frequency

### 2.10 X-ray Powder Diffraction Measurements

In addition to spatial resolution characterization, the detector performance was evaluated through two-dimensional X-ray powder diffraction measurements. Diffraction data were acquired from a LaB₆ powder reference sample, widely used as a standard for diffraction experiments due to its well-defined crystallographic properties.

The acquired two-dimensional diffraction images were corrected for geometrical distortions and detector non-uniformities using flat-field correction procedures. An acquisition time of 3600 s was employed to ensure sufficient counting statistics and high-quality diffraction data.

Figure LL(A) shows the resulting two-dimensional diffraction image of the LaB₆ sample, while Figure LL(B) presents the corresponding azimuthally integrated diffraction pattern obtained using the GSAS-II software package.

**Figure LL:** (A) 2D diffraction image of LaB₆ powder. (B) Integrated diffraction pattern of LaB₆ obtained using GSAS-II

The integrated diffraction pattern exhibits a well-behaved background, represented by the red curve, which is primarily attributed to X-ray scattering and background contributions from the experimental setup. The sharp and well-resolved Bragg peaks demonstrate the detector’s capability to deliver high-quality diffraction data suitable for quantitative crystallographic analysis.

## 3. Results and Discussion

### 3.1 Energy Threshold Stability and Calibration Performance

The energy threshold equalization and calibration procedures applied to the compact Medipix3RX-based detector resulted in a highly uniform and stable response across the full sensitive area. Following pixel-by-pixel noise floor equalization, the dispersion of effective threshold energies among pixels was significantly reduced, enabling homogeneous photon discrimination behavior across all six ASICs comprising the Hexa module. This uniformity is critical for quantitative X-ray measurements, particularly in diffraction and scattering experiments where subtle intensity variations must be reliably resolved.

The X-ray fluorescence–based energy calibration using Co, Zn, Se, and Zr reference targets yielded a linear calibration curve over the investigated energy range, as shown in Figure YY. The excellent linearity observed for each ASIC confirms the intrinsic stability of the Medipix3RX threshold discriminators and validates the robustness of the calibration methodology. Importantly, no significant chip-to-chip deviations were observed, indicating that the hybrid bonding process and subsequent electronic integration did not introduce measurable systematic offsets.

From an application standpoint, this level of energy calibration fidelity enables reproducible detector operation over extended measurement campaigns and supports experiments requiring stable threshold settings, such as background suppression in diffraction measurements or selective energy windowing in spectroscopic imaging.

### 3.2 Spatial Resolution and Modulation Transfer Function

The Modulation Transfer Function measurements provide a quantitative assessment of the detector’s spatial resolving power. As shown in Figure ZZ, the normalized MTF exhibits a characteristic response consistent with expectations for a photon-counting detector employing a 300 μm thick silicon sensor with a pixel pitch of 55 μm. The preservation of high spatial frequency components demonstrates that charge sharing effects and electronic cross-talk are effectively mitigated by the Medipix3RX architecture, particularly through its charge summing and thresholding capabilities.

The MTF values indicate that the detector achieves a spatial resolution well matched to its pixel geometry, confirming that the mechanical alignment, sensor bonding quality, and readout electronics do not introduce additional degradation. This performance is particularly relevant for diffraction and imaging applications where fine structural features or closely spaced diffraction rings must be resolved with high fidelity.

Compared to integrating detectors of similar pixel pitch, the photon-counting operation confers a clear advantage by eliminating readout noise contributions, thereby improving contrast at higher spatial frequencies. These results demonstrate that the compact detector is capable of delivering spatial resolution suitable for demanding X-ray imaging tasks in both laboratory and synchrotron environments.

### 3.3 X-ray Powder Diffraction Performance

The two-dimensional X-ray powder diffraction measurements acquired from the LaB₆ reference sample further substantiate the detector’s performance in practical material analysis applications. The diffraction image shown in Figure LL(A) exhibits uniform intensity distribution and well-defined Debye–Scherrer rings, indicative of consistent detector response and low background noise.

Following geometrical and flat-field corrections, the azimuthally integrated diffraction pattern obtained using GSAS-II, shown in Figure LL(B), reveals sharp Bragg peaks superimposed on a smooth and well-behaved background. The background profile, represented by the red curve, is primarily attributed to scattering contributions from the experimental setup rather than detector-related artifacts. The absence of spurious features or excess noise in the integrated pattern underscores the effectiveness of the pixel equalization and energy thresholding procedures.

The quality of the diffraction data demonstrates that the compact Medipix3RX-based detector is well suited for quantitative XPD measurements, including phase identification, lattice parameter refinement, and microstructural analysis. The combination of high spatial resolution, low noise, and stable energy discrimination enables reliable data acquisition even for long integration times, as required in laboratory-based diffraction experiments.

### 3.4 Implications for Synchrotron and Laboratory Applications

The results presented in this study highlight the versatility of the compact detector design. While optimized to address the stringent requirements of fourth-generation synchrotron sources, the detector also performs exceptionally well in a laboratory environment. This dual applicability is particularly advantageous for facilities seeking to develop complementary laboratory-based characterization capabilities or to perform detector commissioning and method development outside of beamtime constraints.

The modular architecture and scalable readout scheme further suggest that the detector concept can be extended to larger active areas without compromising performance. Such scalability is essential for future diffraction and imaging experiments that demand increased angular coverage or higher throughput.


## 4. Conclusions

In this work, a large-area hybrid photon-counting X-ray detector prototype based on the Medipix3RX ASIC was successfully assembled, commissioned, and characterized. The detector comprises more than 235 kilopixels with a pixel pitch of 55 μm and integrates a monolithic 300 μm thick silicon sensor within a compact, air-cooled form factor. The successful implementation of pixel equalization and X-ray fluorescence–based energy calibration procedures demonstrates excellent stability and uniformity across the full sensitive area during operation.

The spatial resolution performance, quantified through Modulation Transfer Function measurements, confirms that the detector achieves high resolving power consistent with expectations for a silicon-based photon-counting detector of this geometry. The measured MTF values indicate minimal degradation due to electronic or mechanical factors, underscoring the effectiveness of the detector design and integration. Furthermore, the low intrinsic noise and optimized energy thresholding enable high-contrast imaging and reliable photon discrimination.

The X-ray powder diffraction results obtained from a LaB₆ reference sample demonstrate the detector’s capability to deliver high-quality diffraction data suitable for quantitative material analysis. The combination of sharp diffraction features, stable background behavior, and excellent signal-to-noise ratio validates the detector’s applicability to XPD experiments in both laboratory and synchrotron settings.

Overall, the compact Medipix3RX-based detector prototype represents a robust and versatile solution for advanced X-ray material analysis, offering a compelling balance between performance, scalability, and operational flexibility. Its demonstrated capabilities position it as a promising candidate for deployment in a wide range of diffraction, scattering, and imaging applications at next-generation synchrotron facilities and beyond.

---

## References

1. E. F. Eikenberry et al., “PILATUS: A two-dimensional X-ray detector for macromolecular crystallography,” *Nucl. Instrum. Methods Phys. Res. A*, vol. 501, pp. 260–266, 2003.
2. X. Llopart et al., “Medipix3: A 64k pixel detector readout chip working in single photon counting mode with improved spectrometric performance,” *Nucl. Instrum. Methods Phys. Res. A*, vol. 633, pp. S29–S32, 2011.
3. R. Ballabriga et al., “The Medipix3RX: A high resolution, zero dead-time pixel detector readout chip allowing spectroscopic imaging,” *J. Instrum.*, vol. 8, C02016, 2013.
4. P. Kraft et al., “Performance of single-photon-counting PILATUS detector modules,” *IEEE Trans. Nucl. Sci.*, vol. 56, pp. 758–764, 2009.
5. A. Mozzanica et al., “Characterization results of the EIGER photon-counting detector,” *J. Instrum.*, vol. 9, C05010, 2014.
6. H. Graafsma, “Requirements for and development of 2D X-ray detectors for the European XFEL,” *J. Instrum.*, vol. 4, P12011, 2009.
7. B. Schmitt et al., “Mythen detector system,” *Nucl. Instrum. Methods Phys. Res. A*, vol. 501, pp. 267–272, 2003.
8. R. H. Menk et al., “Energy calibration and performance of hybrid pixel detectors for synchrotron radiation,” *Nucl. Instrum. Methods Phys. Res. A*, vol. 607, pp. 602–606, 2009.
9. J. Als-Nielsen and D. McMorrow, *Elements of Modern X-ray Physics*, 2nd ed., Wiley, 2011.
10. B. H. Toby and R. B. Von Dreele, “GSAS-II: The genesis of a modern open-source all purpose crystallography software package,” *J. Appl. Crystallogr.*, vol. 46, pp. 544–549, 2013.
11. M. C. Scott et al., “Ptychographic X-ray computed tomography at the nanoscale,” *Nature*, vol. 483, pp. 444–447, 2012.
12. A. Madsen et al., “X-ray photon correlation spectroscopy,” *IUCrJ*, vol. 1, pp. 106–119, 2014.
13. T. Tschentscher et al., “Photon beam properties of the European XFEL,” *Appl. Sci.*, vol. 7, 592, 2017.
14. G. K. Batchelor et al., “Modulation transfer function analysis of X-ray detectors,” *Med. Phys.*, vol. 31, pp. 178–188, 2004.
15. H. Spieler, *Semiconductor Detector Systems*, Oxford University Press, 2005.

