Grant  RPDC2023-145800-I00 funded by:
![Logos of the Spanish Government, European Union NextGenerationEU, Spanish Recovery and Resilience Plans, and Spanish State Research Agency.](res/MICIU+NextG+PRTR+AEI.svg "Logos")

# FPHUB-RISCV: Floating-Point HUB Unit for RISC-V

## Overview

**FPHUB-RISCV** is an open-source project developing a Floating-Point Unit (FPU) for the **RISC-V** architecture, designed for low-power and resource-constrained applications. This unit is based on the **FPHUB format**, an alternative to IEEE 754 that simplifies hardware complexity while maintaining computational precision.

The **FPHUB format** is a novel floating-point representation that reduces hardware complexity and power consumption while preserving numerical precision. It achieves this by modifying the significand structure, eliminating subnormal numbers, and supporting only rounding-to-nearest, making it an efficient alternative for embedded and low-power computing environments.

## Project Background and Previous Research

In a previous project, we conducted extensive investigations into optimizing floating-point computation. The rounding operation is performed in almost all arithmetic operations involving floating-point (FP) numbers. Among the different rounding modes available in the FP standard (IEEE 754-2008), round-to-nearest (RN) is the predominant mode employed in the majority of FP operations and serves as the default in most processors. However, implementing this rounding mode is costly, often resulting in substantial area and delay overhead due to its placement in the critical path of operations. Recognizing this challenge, numerous researchers have proposed various architectural approaches to mitigate the delay impact, either by merging rounding with other operations or removing it from the critical path.

Another entirely distinct strategy for alleviating the impact of RN involves the utilization of novel real-number encoding and formats, as exemplified in recent research on the HUB (Half-Unit Biased) format. Our proposal, known as HUB, stands out for its ability to simplify arithmetic units at the logic level, offering profound advantages in hardware implementations. The HUB approach concurrently reduces area resources, power consumption, and computation time. Additionally, it has been empirically demonstrated that HUB formats are exceptionally well-suited for general floating-point applications and application-specific fixed-point data paths employing RN.

Our research group has previously undertaken comprehensive investigations into implementing fundamental operations-including addition, subtraction, multiplication, division, and square root-using HUB formats at a laboratory level. Building upon this foundational work, we aim to extend this innovative technique from the laboratory setting to practical, widespread application.

In this line, at the end of our last project, we developed a functional prototype of a floating-point adder designed within a RISC-V architecture. The results of this preliminary research demonstrated the feasibility and potential benefits of integrating specialized arithmetic units within RISC-V processors.

## Licensing & Patents

This project is open-source, but certain aspects of the **FPHUB format** are covered by **Spanish patents** held by the **Universidad de Málaga**. Commercial use within Spain may require a **technology transfer agreement**.

### Patents

- Hormigo, Javier; Villalba-Moreno, Julio. Sumadores coma flotante y conversores, ES2546916B2, 2015. [Link](https://patentscope.wipo.int/search/en/detail.jsf?docId=ES152442316)
- Hormigo, Javier; Villalba-Moreno, Julio. Multiplicadores coma flotante y conversores asociados, ES2546895B2, 2015. [Link](https://patentscope.wipo.int/search/en/detail.jsf?docId=ES152442295)
- Hormigo, Javier; Villalba-Moreno, Julio. Dispositivos para operaciones de multiplicación-suma fusionadas en coma flotante y conversores asociados, ES2546899B2, 2015. [Link](https://patentscope.wipo.int/search/en/detail.jsf?docId=ES152442299)
- Hormigo, Javier; Villalba-Moreno, Julio. Dispositivos coma flotante y conversores, ES2546898B2, 2015. [Link](https://patentscope.wipo.int/search/en/detail.jsf?docId=ES152442298)
- Hormigo, Javier; Villalba-Moreno, Julio. Unidades aritméticas en coma fija y conversores asociados, ES2546915B2, 2015. [Link](https://patentscope.wipo.int/search/en/detail.jsf?docId=ES152442315)

## Acknowledgments

This project is funded by the **Spanish Government** under **Next Generation EU** and supported by the Universidad de Málaga.

## References

The following works form the foundation of this project and represent key contributions in the areas of HUB arithmetic, FPGA implementations, and floating-point optimization in digital signal processing (DSP) and computer architecture:

- Hormigo, J., & Villalba, J. (2015). Optimizing DSP circuits by a new family of arithmetic operators. *Conference Record - Asilomar Conference on Signals, Systems and Computers*, 2015-April, 871–875. [https://doi.org/10.1109/ACSSC.2014.7094576](https://doi.org/10.1109/ACSSC.2014.7094576)

- Hormigo, J., & Villalba, J. (2016). Measuring Improvement When Using HUB Formats to Implement Floating-Point Systems under Round-to-Nearest. *IEEE Transactions on Very Large Scale Integration (VLSI) Systems*, 24(6), 2369–2377. [https://doi.org/10.1109/TVLSI.2015.2502318](https://doi.org/10.1109/TVLSI.2015.2502318)

- Villalba-Moreno, J. (2016). Digit Recurrence Floating-Point Division under HUB Format. *Proceedings - Symposium on Computer Arithmetic*, 2016-September, 79–86. [https://doi.org/10.1109/ARITH.2016.17](https://doi.org/10.1109/ARITH.2016.17)

- Hormigo, J., & Villalba, J. (2017). HUB Floating Point for Improving FPGA Implementations of DSP Applications. *IEEE Transactions on Circuits and Systems II: Express Briefs*, 64(3), 319–323. [https://doi.org/10.1109/TCSII.2016.2563798](https://doi.org/10.1109/TCSII.2016.2563798)

- Villalba-Moreno, J., & Hormigo, J. (2017). Floating point square root under HUB format. *Proceedings - 35th IEEE International Conference on Computer Design, ICCD 2017*, 447–454. [https://doi.org/10.1109/ICCD.2017.79](https://doi.org/10.1109/ICCD.2017.79)

- Villalba-Moreno, J., Hormigo, J., & Gonzalez-Navarro, S. (2018). Unbiased Rounding for HUB Floating-Point Addition. *IEEE Transactions on Computers*, 67(9), 1359–1365. [https://doi.org/10.1109/TC.2018.2807429](https://doi.org/10.1109/TC.2018.2807429)

- Villalba, J., Hormigo, J., & Gonzalez-Navarro, S. (2019). Fast HUB Floating-Point Adder for FPGA. *IEEE Transactions on Circuits and Systems II: Express Briefs*, 66(6), 1028–1032. [https://doi.org/10.1109/TCSII.2018.2873194](https://doi.org/10.1109/TCSII.2018.2873194)

- Villalba-Moreno, J., Hormigo, J., & Jaime, F. (2019). Reproducible Summation under HUB Format. *Proceedings - Symposium on Computer Arithmetic*, 2019-June, 38–45. [https://doi.org/10.1109/ARITH.2019.00015](https://doi.org/10.1109/ARITH.2019.00015)

- Hormigo, J., Villalba-Moreno, J., & Gonzalez-Navarro, S. (2020). Floating-Point Fused Multiply-Add under HUB Format. *Proceedings - Symposium on Computer Arithmetic*, 2020-June, 1–8. [https://doi.org/10.1109/ARITH48897.2020.00010](https://doi.org/10.1109/ARITH48897.2020.00010)

- Garrido, M., Bautista, V. M., Portas, A., & Hormigo, J. (2024). Advanced Quantization Schemes to Increase Accuracy, Reduce Area, and Lower Power Consumption in FFT Architectures. *IEEE Transactions on Circuits and Systems I: Regular Papers*, 1–11. [https://doi.org/10.1109/TCSI.2024.3421348](https://doi.org/10.1109/TCSI.2024.3421348)

- Murillo, R., Hormigo, J., Barrio, A. A. D., & Botella, G. (2024). HUB Meets Posit: Arithmetic Units Implementation. *IEEE Transactions on Circuits and Systems II: Express Briefs, 71*(1), 440–444. [https://doi.org/10.1109/TCSII.2023.3307488](https://doi.org/10.1109/TCSII.2023.3307488)

- Bandera, G., Salamero, J., Moreto, M., & Villalba, J. (2024). Floating Point HUB Adder for RISC-V Sargantana Processor. *arXiv preprint* arXiv:2401.09464. [https://arxiv.org/abs/2401.09464v1](https://arxiv.org/abs/2401.09464v1)

- Hormigo, J., & Muñoz, S. D. (2021). Efficient Floating-Point Givens Rotation Unit. *Circuits, Systems, and Signal Processing, 40*(5), 2419–2442. [https://doi.org/10.1007/S00034-020-01580-X](https://doi.org/10.1007/S00034-020-01580-X)

- Hormigo, J., & Villalba, J. (2015). Simplified floating-point units for high dynamic range image and video systems. *Proceedings of the International Symposium on Consumer Electronics, ISCE*, 2015-August. [https://doi.org/10.1109/ISCE.2015.7177797](https://doi.org/10.1109/ISCE.2015.7177797)

- Munoz, S. D., & Hormigo, J. (2015). Improving fixed-point implementation of QR decomposition by rounding-to-nearest. *Proceedings of the International Symposium on Consumer Electronics, ISCE*, 2015-August. [https://doi.org/10.1109/ISCE.2015.7177822](https://doi.org/10.1109/ISCE.2015.7177822)

- Hormigo, J., & Villalba, J. (2016). New formats for computing with real-numbers under round-to-nearest. *IEEE Transactions on Computers, 65*(7), 2158–2168. [https://doi.org/10.1109/TC.2015.2479623](https://doi.org/10.1109/TC.2015.2479623)

