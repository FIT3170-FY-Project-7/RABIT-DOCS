
# Posterior LaTeX Labels

RABIT features a set of predefined LaTeX labels for certain parameters. The following is a table showing the Bilby outputted parameter, and its corresponding LaTeX label in RABIT:

Key:

- Posterior Name: The name of the posterior parameter in a Bilby-outputted JSON file
- Posterior Label: Unrendered LaTeX of the posterior's label
- Unit Label: Unrendered LaTeX of the posterior's units (if available)
- Full LaTeX Label: Rendered LaTeX combining the posterior's label and unit label. This is the label that is used in RABIT

| Posterior name           | Posterior label          | Unit label  | Full LaTeX label                     |
| ------------------------ | ------------------------ | ----------- | ------------------------------------ |
| `chirp_mass`             | `\mathcal{M}`            | `M_{\odot}` | \\(\mathcal{M} \ [M_{\odot}]\\)      |
| `mass_ratio`             | `q`                      |             | \\(q\\)                              |
| `mass_1`                 | `m_1^{\rm Lab}`          | `M_{\odot}` | \\(m_1^{\rm Lab} \ [M_{\odot}]\\)    |
| `mass_2`                 | `m_2^{\rm Lab}`          | `M_{\odot}` | \\(m_2^{\rm Lab} \ [M_{\odot}]\\)    |
| `total_mass`             | `M^{\rm Lab}`            | `M_{\odot}` | \\(M^{\rm Lab} \ [M_{\odot}]\\)      |
| `mass_1_source`          | `m_1^{\rm Source}`       | `M_{\odot}` | \\(m_1^{\rm Source} \ [M_{\odot}]\\) |
| `mass_2_source`          | `m_2^{\rm Source}`       | `M_{\odot}` | \\(m_2^{\rm Source} \ [M_{\odot}]\\) |
| `total_mass_source`      | `M^{\rm Source}`         | `M_{\odot}` | \\(M^{\rm Source} \ [M_{\odot}]\\)   |
| `a_1`                    | `a_1`                    |             | \\(a_1\\)                            |
| `a_2`                    | `a_2`                    |             | \\(a_2\\)                            |
| `tilt_1`                 | `\theta_1`               | `{\rm rad}` | \\(\theta_1 \ [{\rm rad}]\\)         |
| `tilt_2`                 | `\theta_2`               | `{\rm rad}` | \\(\theta_2 \ [{\rm rad}]\\)         |
| `cos_tilt_1`             | `\cos{\theta_1}`         |             | \\(\cos{\theta_1}\\)                 |
| `cos_tilt_2`             | `\cos{\theta_2}`         |             | \\(\cos{\theta_2}\\)                 |
| `phi_12`                 | `\phi_{12}`              | `{\rm rad}` | \\(\phi_{12} \ [{\rm rad}]\\)        |
| `phi_jl`                 | `\phi_{\rm JL}`          | `{\rm rad}` | \\(\phi_{\rm JL} \ [{\rm rad}]\\)    |
| `luminosity_distance`    | `d_{\rm L}`              | `{\rm Mpc}` | \\(d_{\rm L} \ [{\rm Mpc}]\\)        |
| `ra`                     | `{\rm RA}`               | `{\rm rad}` | \\({\rm RA} \ [{\rm rad}]\\)         |
| `theta_jn`               | `\theta_{JN}`            | `{\rm rad}` | \\(\theta_{JN} \ [{\rm rad}]\\)      |
| `cos_theta_jn`           | `\cos{\theta_{JN}}`      |             | \\(\cos{\theta_{JN}}\\)              |
| `psi`                    | `\psi`                   | `{\rm rad}` | \\(\psi \ [{\rm rad}]\\)             |
| `phase`                  | `\phi`                   | `{\rm rad}` | \\(\phi \ [{\rm rad}]\\)             |
| `phi_1`                  | `\phi_1`                 |             | \\(\phi_1\\)                         |
| `phi_2`                  | `\phi_1`                 |             | \\(\phi_1\\)                         |
| `geocent_time`           | `t_c`                    | `{\rm s}`   | \\(t_c \ [{\rm s}]\\)                |
| `azimuth`                | `\epsilon`               | `{\rm rad}` | \\(\epsilon \ [{\rm rad}]\\)         |
| `zenith`                 | `\kappa`                 | `{\rm rad}` | \\(\kappa \ [{\rm rad}]\\)           |
| `iota`                   | `\iota`                  | `{\rm rad}` | \\(\iota \ [{\rm rad}]\\)            |
| `cos_iota`               | `\cos{\iota}`            |             | \\(\cos{\iota}\\)                    |
| `redshift`               | `z`                      |             | \\(z\\)                              |
| `eccentricity`           | `e`                      |             | \\(e\\)                              |
| `dec`                    | `{\rm DEC}`              | `{\rm rad}` | \\({\rm DEC} \ [{\rm rad}]\\)        |
| `chi_1`                  | `\chi_1`                 |             | \\(\chi_1\\)                         |
| `chi_2`                  | `\chi_2`                 |             | \\(\chi_2\\)                         |
| `chi_1_in_plane`         | `\chi_1^{\perp}`         |             | \\(\chi_1^{\perp}\\)                 |
| `chi_2_in_plane`         | `\chi_2^{\perp}`         |             | \\(\chi_2^{\perp}\\)                 |
| `chi_eff`                | `\chi_{\rm eff}`         |             | \\(\chi_{\rm eff}\\)                 |
| `chi_p`                  | `\chi_{\rm p}`           |             | \\(\chi_{\rm p}\\)                   |
| `spin_1x`                | `S_{1,x}`                |             | \\(S_{1,x}\\)                        |
| `spin_1y`                | `S_{1,y}`                |             | \\(S_{1,y}\\)                        |
| `spin_1z`                | `S_{1,z}`                |             | \\(S_{1,z}\\)                        |
| `spin_2x`                | `S_{2,x}`                |             | \\(S_{2,x}\\)                        |
| `spin_2y`                | `S_{2,y}`                |             | \\(S_{2,y}\\)                        |
| `spin_2z`                | `S_{2,z}`                |             | \\(S_{2,z}\\)                        |
| `comoving_distance`      | `d_{\rm C}`              | `{\rm Mpc}` | \\(d_{\rm C} \ [{\rm Mpc}]\\)        |
| `symmetric_mass_ratio`   | `\eta`                   |             | \\(\eta\\)                           |
| `lambda_1`               | `\Lambda_1`              |             | \\(\Lambda_1\\)                      |
| `lambda_2`               | `\Lambda_2`              |             | \\(\Lambda_2\\)                      |
| `lambda_tilde`           | `\tilde{\Lambda}`        |             | \\(\tilde{\Lambda}\\)                |
| `delta_lambda_tilde`     | `\delta \tilde{\Lambda}` |             | \\(\delta \tilde{\Lambda}\\)         |
| `H1_time`                | `t_H`                    | `{\rm s}`   | \\(t_H \ [{\rm s}]\\)                |
| `time_jitter`            | `\delta t`               | `{\rm s}`   | \\(\delta t \ [{\rm s}]\\)           |
| `recalib_H1_amplitude_0` | `A^{H1}_0`               |             | \\(A^{H1}_0\\)                       |
| `recalib_H1_amplitude_1` | `A^{H1}_1`               |             | \\(A^{H1}_1\\)                       |
| `recalib_H1_amplitude_2` | `A^{H1}_2`               |             | \\(A^{H1}_2\\)                       |
| `recalib_H1_amplitude_3` | `A^{H1}_3`               |             | \\(A^{H1}_3\\)                       |
| `recalib_H1_amplitude_4` | `A^{H1}_4`               |             | \\(A^{H1}_4\\)                       |
| `recalib_H1_amplitude_5` | `A^{H1}_5`               |             | \\(A^{H1}_5\\)                       |
| `recalib_H1_amplitude_6` | `A^{H1}_6`               |             | \\(A^{H1}_6\\)                       |
| `recalib_H1_amplitude_7` | `A^{H1}_7`               |             | \\(A^{H1}_7\\)                       |
| `recalib_H1_amplitude_8` | `A^{H1}_8`               |             | \\(A^{H1}_8\\)                       |
| `recalib_H1_amplitude_9` | `A^{H1}_9`               |             | \\(A^{H1}_9\\)                       |
| `recalib_H1_phase_0`     | `\phi^{H1}_0`            |             | \\(\phi^{H1}_0\\)                    |
| `recalib_H1_phase_1`     | `\phi^{H1}_1`            |             | \\(\phi^{H1}_1\\)                    |
| `recalib_H1_phase_2`     | `\phi^{H1}_2`            |             | \\(\phi^{H1}_2\\)                    |
| `recalib_H1_phase_3`     | `\phi^{H1}_3`            |             | \\(\phi^{H1}_3\\)                    |
| `recalib_H1_phase_4`     | `\phi^{H1}_4`            |             | \\(\phi^{H1}_4\\)                    |
| `recalib_H1_phase_5`     | `\phi^{H1}_5`            |             | \\(\phi^{H1}_5\\)                    |
| `recalib_H1_phase_6`     | `\phi^{H1}_6`            |             | \\(\phi^{H1}_6\\)                    |
| `recalib_H1_phase_7`     | `\phi^{H1}_7`            |             | \\(\phi^{H1}_7\\)                    |
| `recalib_H1_phase_8`     | `\phi^{H1}_8`            |             | \\(\phi^{H1}_8\\)                    |
| `recalib_H1_phase_9`     | `\phi^{H1}_9`            |             | \\(\phi^{H1}_9\\)                    |
| `recalib_H1_frequency_0` | `f^{H1}_0`               | `{\rm Hz}`  | \\(f^{H1}_0 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_1` | `f^{H1}_1`               | `{\rm Hz}`  | \\(f^{H1}_1 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_2` | `f^{H1}_2`               | `{\rm Hz}`  | \\(f^{H1}_2 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_3` | `f^{H1}_3`               | `{\rm Hz}`  | \\(f^{H1}_3 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_4` | `f^{H1}_4`               | `{\rm Hz}`  | \\(f^{H1}_4 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_5` | `f^{H1}_5`               | `{\rm Hz}`  | \\(f^{H1}_5 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_6` | `f^{H1}_6`               | `{\rm Hz}`  | \\(f^{H1}_6 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_7` | `f^{H1}_7`               | `{\rm Hz}`  | \\(f^{H1}_7 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_8` | `f^{H1}_8`               | `{\rm Hz}`  | \\(f^{H1}_8 \ [{\rm Hz}]\\)          |
| `recalib_H1_frequency_9` | `f^{H1}_9`               | `{\rm Hz}`  | \\(f^{H1}_9 \ [{\rm Hz}]\\)          |
| `recalib_L1_amplitude_0` | `A^{L1}_0`               |             | \\(A^{L1}_0\\)                       |
| `recalib_L1_amplitude_1` | `A^{L1}_1`               |             | \\(A^{L1}_1\\)                       |
| `recalib_L1_amplitude_2` | `A^{L1}_2`               |             | \\(A^{L1}_2\\)                       |
| `recalib_L1_amplitude_3` | `A^{L1}_3`               |             | \\(A^{L1}_3\\)                       |
| `recalib_L1_amplitude_4` | `A^{L1}_4`               |             | \\(A^{L1}_4\\)                       |
| `recalib_L1_amplitude_5` | `A^{L1}_5`               |             | \\(A^{L1}_5\\)                       |
| `recalib_L1_amplitude_6` | `A^{L1}_6`               |             | \\(A^{L1}_6\\)                       |
| `recalib_L1_amplitude_7` | `A^{L1}_7`               |             | \\(A^{L1}_7\\)                       |
| `recalib_L1_amplitude_8` | `A^{L1}_8`               |             | \\(A^{L1}_8\\)                       |
| `recalib_L1_amplitude_9` | `A^{L1}_9`               |             | \\(A^{L1}_9\\)                       |
| `recalib_L1_phase_0`     | `\phi^{L1}_0`            |             | \\(\phi^{L1}_0\\)                    |
| `recalib_L1_phase_1`     | `\phi^{L1}_1`            |             | \\(\phi^{L1}_1\\)                    |
| `recalib_L1_phase_2`     | `\phi^{L1}_2`            |             | \\(\phi^{L1}_2\\)                    |
| `recalib_L1_phase_3`     | `\phi^{L1}_3`            |             | \\(\phi^{L1}_3\\)                    |
| `recalib_L1_phase_4`     | `\phi^{L1}_4`            |             | \\(\phi^{L1}_4\\)                    |
| `recalib_L1_phase_5`     | `\phi^{L1}_5`            |             | \\(\phi^{L1}_5\\)                    |
| `recalib_L1_phase_6`     | `\phi^{L1}_6`            |             | \\(\phi^{L1}_6\\)                    |
| `recalib_L1_phase_7`     | `\phi^{L1}_7`            |             | \\(\phi^{L1}_7\\)                    |
| `recalib_L1_phase_8`     | `\phi^{L1}_8`            |             | \\(\phi^{L1}_8\\)                    |
| `recalib_L1_phase_9`     | `\phi^{L1}_9`            |             | \\(\phi^{L1}_9\\)                    |
| `recalib_L1_frequency_0` | `f^{L1}_0`               | `{\rm Hz}`  | \\(f^{L1}_0 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_1` | `f^{L1}_1`               | `{\rm Hz}`  | \\(f^{L1}_1 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_2` | `f^{L1}_2`               | `{\rm Hz}`  | \\(f^{L1}_2 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_3` | `f^{L1}_3`               | `{\rm Hz}`  | \\(f^{L1}_3 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_4` | `f^{L1}_4`               | `{\rm Hz}`  | \\(f^{L1}_4 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_5` | `f^{L1}_5`               | `{\rm Hz}`  | \\(f^{L1}_5 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_6` | `f^{L1}_6`               | `{\rm Hz}`  | \\(f^{L1}_6 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_7` | `f^{L1}_7`               | `{\rm Hz}`  | \\(f^{L1}_7 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_8` | `f^{L1}_8`               | `{\rm Hz}`  | \\(f^{L1}_8 \ [{\rm Hz}]\\)          |
| `recalib_L1_frequency_9` | `f^{L1}_9`               | `{\rm Hz}`  | \\(f^{L1}_9 \ [{\rm Hz}]\\)          |
