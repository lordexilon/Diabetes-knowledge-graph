# Diabetes Knowledge Graph Data
## 一、Data Sources
The data comes from the Tianchi competition platform, link address: https://tianchi.aliyun.com/dataset/dataDetail?spm=5176.12281978.0.0.7592412fAyjFC6&dataId=22288
To obtain the original data, please go to the Tianchi platform to download.

## Entity types are:
* Disease related:

1. Disease name (Disease), such as type I diabetes.
2. Etiology (Reason), the cause, risk factors and mechanism of the disease. For example, "diabetes is caused by insulin resistance", insulin resistance is the cause.
3. Clinical manifestations (Symptom), including symptoms, signs, direct manifestations of patients and judgments that require a doctor's physical examination. Such as "dizziness" "blood in stool" and so on.
4. Inspection methods (Test), including laboratory inspection methods, imaging inspection methods, auxiliary tests, items with diagnostic and differential significance for diseases, such as triglycerides.
5. Check the index value (Test_Value), the specific value of the index, negative and positive, presence or absence, increase or decrease, high or low, etc., such as ">11.3 mmol/L".

* Treatment related:

6. The name of the drug (Drug), including conventional drugs and chemotherapy drugs, such as insulin.
7. Frequency of medication (Frequency), including frequency of medication and frequency of symptoms, such as twice a day.
8. The dosage (Amount), such as 500mg/d.
9. Medication method (Method): such as morning and evening, before and after meals, oral, intravenous injection, inhalation, etc.
10. Non-drug treatment (Treatment), non-drug treatment carried out in a hospital environment, including radiotherapy, traditional Chinese medicine treatment methods, etc., such as massage, massage, acupuncture, physical therapy, excluding diet, exercise, nutrition, etc.
11. Operation, including the name of the operation, such as metabolic surgery, etc.
12. Adverse reactions (SideEff), adverse reactions after medication.
* Regular entities:

13. Anatomy, including anatomical parts and biological tissues, such as various parts and organs of the human body, and pancreatic islet cells.
14. Level (level), including the severity of the disease, the degree of remission after treatment, etc.
15. Duration (Duration), including symptom duration and medication duration, such as "one week" in "dizziness for one week".

## Relationship type
Entity relationship class name
1. Test Method -> Disease (Test_Disease)
2. Clinical manifestation -> disease (Symptom_Disease)
3. Non-drug treatment -> disease (Treatment_Disease)
4. Drug Name -> Disease (Drug_Disease)
5. Part -> Disease (Anatomy_Disease)
6. Medication Frequency -> Drug Name (Frequency_Drug)
7. Duration -> Drug Name (Duration_Drug)
8. Dosage -> Drug Name (Amount_Drug)
9. Medication method -> drug name (Method_Drug)
10. Adverse reactions -> drug name (SideEff-Drug)

## 2. Data scale
After the data is processed, there are 15778 entities and 40060 relationships

## 3. Data set description
* There are two folders under the diabetes_kg_data folder, namely cate_ent (entity folder), cate_rel (relationship folder), and the files are all CSV types
* The 15 files under the entity folder correspond to each entity type. Each file has three columns ent_id, ent_name, and category, which are entity ID, entity name, and entity category
* There are 10 files under the relationship folder, corresponding to each relationship type, each file has three columns from, to, rel, which are the head node entity, tail node entity and entity relationship type
