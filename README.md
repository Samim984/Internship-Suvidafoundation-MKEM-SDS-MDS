🧠 Multi-Knowledge-Enhanced Model (MKEM) framework applied to both Single-Document    
                 Summarization (SDS) and Multi-Document Summarization (MDS)⬇️

⌛In an age where the world produces more news in a single day than a human can read in a lifetime, the ability to distill vast information into concise, meaningful summaries is no longer a luxury—it is a necessity. This thesis presents the Multi-Knowledge-Enhanced Model (MKEM) framework applied to both Single-Document Summarization (SDS) and Multi-Document Summarization (MDS).🧮

📚MKEM story👇

<img width="1536" height="1024" alt="MEKM FrameWork" src="https://github.com/user-attachments/assets/064d0e10-7967-4c85-a2fe-b09769d230e2" />
📚Introduction

<img width="590" height="463" alt="Dataset Taxonomy" src="https://github.com/user-attachments/assets/12c56778-7c1e-4a9f-870c-fb78cf09325b" />

✏️NewsSum (IndianNewsPaper-DataSet)

<img width="692" height="442" alt="NewsSum Dataset" src="https://github.com/user-attachments/assets/24c38342-7ef0-401c-a53b-74ef0c0984dc" />

<img width="590" height="463" alt="Dataset Taxonomy" src="https://github.com/user-attachments/assets/b1a27757-d96f-449e-a654-1f8802f51d36" />

💡 Modeling Steps

<img width="878" height="175" alt="Modeling Steps" src="https://github.com/user-attachments/assets/7cc60198-c58c-4f8d-8795-4ff2cd67e6ae" />

🎯 Execution Plan

<img width="734" height="175" alt="Execution Plan" src="https://github.com/user-attachments/assets/fc5c93fe-edf3-40b1-84fd-9e1d24ef6d9a" />

🧮Count of models🎰 run on that dataset

<img width="707" height="424" alt="Model Implemetation count by DataSets" src="https://github.com/user-attachments/assets/365f3a9b-e1bc-4f55-8747-5f914c32a4dd" />

🔍Successfully merged 22 CSV files containing model scores on different datasets.

Each model-dataset pair has ROUGE and BERTScore metrics, inference times, and resource usage data.

Observation: The dataset reveals that most models have been tested on standard SDS datasets (CNN DailyMail, XSum) as well as the MDS dataset (NewsSum). This comprehensive benchmarking across datasets allows analysis of how models scale from single to multi-document summarization.

<img width="665" height="514" alt="All The DataSets +Model Result" src="https://github.com/user-attachments/assets/2a422c10-029b-425f-a713-e89d705797ee" />

🔍Observation:
The table consolidates the trade-offs, showing that the best model depends on the use case:

For accuracy in MDS tasks (NewsSum), PRIMERA and FLAN-T5 lead.

For speed in SDS tasks (CNN DailyMail), T5 and PEGASUS provide faster results with reasonable accuracy.

GPU usage is mostly marked as CPU in this dataset, implying room for improvement in runtime if GPU acceleration is applied.

1️⃣Performance Gap Between SDS and MDS per Model

<img width="568" height="424" alt="ROUGE L score by SDS MDS" src="https://github.com/user-attachments/assets/9a819761-26df-4551-8acd-1c9e5a150e17" />
<img width="431" height="280" alt="ROUGE L performance by SDS MDS" src="https://github.com/user-attachments/assets/f5162750-5ad3-439b-9d7c-b0160a1cef52" />
🔍 Observation 1:
Performance gap between SDS and MDS summarization tasks varies significantly by model.
Models like PRIMERA and FLAN-T5 show higher ROUGE-L scores on MDS datasets (NewsSum, MultiNews) compared to SDS datasets (CNN DailyMail, XSum), indicating they are better at handling long, multi-document inputs.
Conversely, models such as T5 and PEGASUS perform very well on SDS datasets but show a noticeable drop in performance on MDS datasets.
This suggests that model architectures or training strategies influence their capability to summarize longer, more complex document collections, which is crucial for multi-document summarization tasks like Indian news aggregation.
2️⃣Models Handling Long Documents (MDS) Better
<img width="565" height="424" alt="Average ROUGE L SDS" src="https://github.com/user-attachments/assets/a57b0c99-04ce-4e3a-aaba-996bcc9a1088" />
🔍 Observation 2:
There is a noticeable trade-off between inference speed and accuracy across models. While models like PEGASUS and T5 have relatively faster inference times, they sometimes show lower ROUGE-L scores on longer documents. On the other hand, models like LED and PRIMERA, though slower, tend to deliver higher accuracy, indicating a balance needs to be struck depending on application needs (real-time vs quality-focused summarization).
3️⃣Speed vs Accuracy Balance (Inference Time vs ROUGE-L)
<img width="563" height="352" alt="Inference time vs Roug L" src="https://github.com/user-attachments/assets/6c7b80d5-1181-4dc3-9b97-39d6df3ae8c8" />
🔍 Observation 3:¶
Computational resources (CPU vs GPU) impact both runtime and feasibility of model deployment. Although most experiments ran on CPU in your data, models designed to leverage GPUs show potential for significantly reduced inference times, which is critical for scaling summarization in real-world applications.
4️⃣ Impact of Computational Resources (GPU vs CPU)
<img width="568" height="424" alt="Model by Computational Resource" src="https://github.com/user-attachments/assets/dceebcc0-96c0-453c-a2da-d84a99c079fe" />
<img width="424" height="280" alt="ROUGE L distribution by Computational Resource" src="https://github.com/user-attachments/assets/b3a0a303-ec3d-445d-b393-57565a37a2e8" />
🔍 Observation 4:¶
The performance gap between SDS and MDS summarization varies by model: Some models maintain relatively stable performance across both SDS and MDS datasets, while others show significant drops on MDS datasets. This highlights the importance of selecting models based on the document complexity and length inherent in the target summarization task.






