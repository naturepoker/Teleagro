# Teleagro


---


            ,@##          %..      %#/            
             &%/          %,.      %#/            
            *&%.          %..      %#(            
            (%%           %..      %#(            
            /%%           %*.      %#(            
             %%            &#.,*,(###.            
             #%                %,(                
             #%/               %,(                
            .%%(               %,/                
             #%%%%#%%%#%(./(*,**#(                
                       #*,                        
                       .%,.                       
                        %,#                       
                        %,%                       
                        %#%                       
                       (%%%                       
                        (%                                                                          
                 
           Binomica Labs - TeleAgro         
              
           Small Thoughtful Science             


---

Teleagro is a script suite for screening NCBI refseq Agrobacteria genomes for similar proteins and phylogeny among genomes.
This script is meant to provide a **bird's eye view** for a researcher who needs a jumping off point for a research question! 
As such, the output will always be a little rough, requiring some degree of search and screening.
For example, during HMM scan the script does not make a distinction between top-scoring HMM profile match versus lower scoring ones. 

Simply clone or download the folder, and execute the Teleagro.sh script followed by a protein fasta file of your choice. 

`./Teleagro.sh myown.faa`

The script will download and setup the necessary Pfam and Taxonkit dump file if necessary, and point out any missing dependencies. 

Once finished, the script will produce a folder named TA_output containing about 12 files including:

- Pfam screening result of the submitted protein
- Genbank accession list of all ncbi agrobacteria proteins that belongs to the same Pfam group
- Annotation of the agrobacteria proteins accessions
- .seq file containing all the protein sequences of the agrobacteria proteins
- .seq file containing the CDS nucleotide sequences of the agrobacteria proteins, along with their coordinates 
- .aln Muscle alignment of all agrobacteria proteins that belong to the Pfam group of your protein of interest
- .tre FastTree cladogram of the similarity/distance between the agrobacteria protein sequences 
- .txt files containing taxonomic info and lineage on all agrobacteria that contain the proteins processed above

---

**Dependencies**

HMMER and Entrez-Direct are absolute requirements. 

It is highly recommended that you have Muscle, FastTree, and Taxonkit installed on your system path already. 
However, if the script fails to detect any of the required three programs it will use the binaries included in the directory. 
