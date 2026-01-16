INTRODUCTION

Salmonella is a highly prevalent foodborne pathogen which poses great concern to global health. Salmonella can cause conditions such as gastroenteritis which consists of symptoms such as  fever, diarrhea and abdominal cramps. There are more than 2600 serotypes of Salmonella enterica, each being distinguished by differences in their surface antigens (Mileto et al., 2025).
Whole genome sequencing (WGS) has become substantially more affordable and accessible due  to the introduction of Next Generation Sequencing (NGS), and due to the overall decrease of sequencing expenses. The use of WGS for Salmonella serotyping offers enhanced discriminatory power, even compared to gold-standard agglutination practices. Prior studies have used WGS for Salmonella serotyping, and have verified its reliability, performance, and applicability. It has been shown to be a viable alternative to other well understood phenotypic methods (Mileto et al., 2025). These previous studies display the ability of WGS to yield accurate and high-throughput prediction of serotypes, and in addition, facilitate large-scale epidemiological studies.
Advances in long-read sequencing technologies, such as Oxford Nanopore sequencing, have provided the capability of assembling complete plasmids, which are often difficult to elucidate using short-read data alone. Long-reads are particularly valuable for characterizing genetic elements such as multidrug resistance plasmids, which play a key role in the spread of antimicrobial resistance in bacterial populations (Zhao et al., 2023).
Due to the Oxford Nanopore R10 technology, generation of accurate de novo assemblies of bacterial genomes can now be generated using solely long-read data. (Zhao et al., 2023). Additionally, with appropriate sequencing depth, Nanopore assemblies reach high accuracy which renders them suitable for epidemiological analyses (Zhao et al., 2023). This is a valuable leap in technological capabilities, as it effectively replaces the short/long -read hybrid approaches, which reduces cost and turnaround time. 
Genome sequencing does not simply produce a complete and accurate genome. Because the DNA is broken up into various short and imperfect reads which requires careful reconstruction, often by computer. De novo genome assembly is the process of accurately reconstructing the genome, starting with small over-lapping reads (Wick et al., 2023). The quality of a specific assembly is described by two factors. The first being accuracy, which describes errors in the assembled sequence, the second is completeness, which describes how fragmented the assembly is relative to the real genome (Wick et al., 2023). For bacterial genomes, the desired outcome is one contig per plasmid or chromosome. This, however, is often difficult due to the common presence of repeated sequences, and structural complexity in bacterial genomes. These attributes often lead to ambiguities and errors during assembly. Despite that low-quality assemblies may be applicable for basic tasks, analyses pertaining to mutations, transmission tracking, and whole-genome alignment, demand a highly accurate assembly. This is because even small errors can drastically impact biological interpretations and conclusions (Wick et al., 2023). 
Oxford Nanopore sequencing yields long-reads which can then be used to assemble bacterial genomes. However, the reads may contain methodologically induced errors, which can affect the accuracy of the assembly downstream. For example, the MinION platform showed a quite high alignment identity, but errors were common, however. The errors mostly consisted of insertions and deletions, with many of them occurring in homopolymer regions (Tyler et al., 2018). Wick et al. state that although long-reads improve completeness of an assembly, most long-read assemblies still contain errors. Small errors can often be corrected through polishing processes, large structural errors may still exist if introduced during assembly (Wick et al., 2023). Because homopolymers are especially difficult for Nanopore sequencing to resolve, further refining and validation steps are necessary to ensure accuracy levels required for genomic analysis (Wick et al., 2023). 
Short-read and long-read sequencing are typically both used in traditional genome assembly workflows. This is because short-reads have a high base-calling accuracy, and long-reads show overall architecture and continuity over certain repeats or motifs. However, this increases the cost and turnaround time (Zhao et al., 2023). Recent experiments using Oxford Nanopore with R10 flow cell produced long-read data with greatly improved accuracy of 98.9%, which allows de novo assembly using long-reads only (Zhao et al., 2023). Utilizing the Flye assembler and Medaka software, bacterial genomes of 5 Mb can reach levels of >99.99% accuracy, yielding a complete genome without the need for short-read data (Zhao et al., 2023). Wick et al. also discuss a long-read workflow where they’re used to build the framework of the assembly, followed by polishing procedures to correct remaining errors (Wick et al., 2023).  
When using Nanopore reads to assemble bacterial genomes, it is necessary to evaluate it’s accuracy due to potential inaccuracies being present. To do this, assembled genomes are aligned to a reference genome, of high quality. This provides the standard which is used to identify inaccuracies. Assemblies are compared to the reference genome using sequence alignment. Zhao et al. created reference genomes using traditional methods of combining long-read and short-read data, along with multiple rounds of polishing. These constructs are highly accurate and can be taken as an accurate reference (Zhao et al., 2023). Nanopore assembled genomes were then aligned to these reference genomes to identify insertions, deletions, and single-nucleotide variations. These constitute the main assembly errors when using Nanopore methods, and counting them describes the accuracy of a given assembly (Zhao et al., 2023).  Alignment subsequently provides a way to analyze if an assembly, and the following polishing steps, have produced a genome that describes the true sequence (Wick et al., 2023). 
In this study, Nanopore sequencing data from Salmonella enterica will be utilized to generate a de novo genome assembly, which will then be compared to a reference genome so its accuracy may be evaluated. Long-read sequences will be assembled, followed by polishing steps to reduce errors. The assemblies will then be aligned to a high-quality reference genome obtained form NCBI. Alignment results will then be visualized to allow assessment for both structural, and base-level differences between the constructed assemblies and the reference. This project aims to display how effectively Nanopore based genome assembly can yield reliable and high quality genomes, which are suitable for downstream analysis. 




METHODS

Nanopore long-read sequencing data from Salmonella enterica will serve as a starting point for genome assembly. First, the raw reads will be subject to quality control measures to remove low quality and short sequences, before assembly begins. The now filtered reads will be assembled de novo using the Flye assembler, which is optimal for long-read genome reconstruction (Zhao et al., 2023). The assemblies will then be refined and polished using Medaka to reduce base-level errors, which are commonly associated with Nanopore sequencing. Assembly accuracy will be evaluated by performing an alignment between the polished genome, and a high-quality reference genome from NCBI (Zhao et al., 2023). The alignment results will then be visualized in order to assess the sequence accuracy (Wick et al., 2023)


























References

Mileto, I., Romano, G., Gaiarsa, S., Grassia, G., Bagnarino, J., Piralla, A., Monzillo, V., Cambieri, P., Baldanti, F., & Corbella, M. (2025). Whole genome sequencing as a reliable alternative for salmonella serotyping: A comparative study with the gold-standard method. Frontiers in Microbiology, 16. https://doi.org/10.3389/fmicb.2025.1685741 

Zhao, W., Zeng, W., Pang, B., Luo, M., Peng, Y., Xu, J., Kan, B., Li, Z., & Lu, X. (2023). Oxford nanopore long-read sequencing enables the generation of complete bacterial and plasmid genomes without short-read sequencing. Frontiers in Microbiology, 14. https://doi.org/10.3389/fmicb.2023.1179966 

Wick, R. R., Judd, L. M., & Holt, K. E. (2023). Assembling the perfect bacterial genome using Oxford Nanopore and Illumina sequencing. PLOS Computational Biology, 19(3). https://doi.org/10.1371/journal.pcbi.1010905 

Tyler, A. D., Mataseje, L., Urfano, C. J., Schmidt, L., Antonation, K. S., Mulvey, M. R., & Corbett, C. R. (2018). Evaluation of Oxford Nanopore’s minion sequencing device for microbial whole genome sequencing applications. Scientific Reports, 8(1). https://doi.org/10.1038/s41598-018-29334-5 
