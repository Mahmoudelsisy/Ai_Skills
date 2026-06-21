# Bioinformatics & Health Tech Engineering | المعلوماتية الحيوية وهندسة التقنيات الصحية

## Arabic Description | وصف بالعربية
قواعد صارمة لتطوير البرمجيات في مجالات المعلوماتية الحيوية (Bioinformatics) والتقنيات الصحية (Health Tech). تركز هذه القواعد على دقة البيانات الجينية، الامتثال للمعايير الطبية (HL7/FHIR)، وأمان البيانات الحساسة.

---

## Strict Rules | قواعد صارمة

### 1. Data Accuracy & Integrity
- **Genomic Data Standards**: Follow established formats (FASTA, FASTQ, BAM, VCF) for genomic data.
- **Validation**: Implement rigorous validation for clinical data to prevent errors in medical decision-making.

### 2. Interoperability (HL7/FHIR)
- **FHIR Standards**: Use the HL7 FHIR (Fast Healthcare Interoperability Resources) standard for exchanging electronic health records.
- **RESTful API for Health**: Implement healthcare APIs that are secure and compliant with interoperability regulations.

### 3. Medical Device Software (SaMD)
- **IEC 62304 Compliance**: Follow IEC 62304 standards for the lifecycle of medical device software.
- **Risk Management**: Conduct thorough risk analysis for any software that directly impacts patient care.

### 4. Privacy & HIPAA (Advanced)
- **De-identification**: ALWAYS de-identify patient data before using it for research or training AI models.
- **Audit Logging**: Maintain comprehensive, immutable logs of all accesses to Protected Health Information (PHI).

### 5. Algorithmic Reliability
- **Clinical Validation**: Any algorithm used for diagnosis or treatment MUST be clinically validated.
- **Reproducibility**: Ensure all bioinformatics pipelines are fully reproducible (e.g., using Nextflow or Snakemake).
