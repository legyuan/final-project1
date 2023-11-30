# final Kaggle project1:

Describe Your Dataset:
URL: https://www.kaggle.com/datasets/emmanuelfwerr/thyroid-disease-data/data

Task:

환자의 정보(나이) 및 검사수치 데이터 등을 활용하여
갑상선 질환에 대한 진단

Datasets

thyroidDf 데이터세트는 UCI Machine Learning Repository에서 제공한 갑상선 질환 데이터세트를 조정하여 생성

파일 : thyroidDF.csv- 9,172개 관측치 x 31개 속성

관측치 중 일부를 제외하고, 실제는 7,675개의 관측치를 3개의 셋으로 나눔

학습 데이터: 4,000 개의 환자 정보

검증 데이터: 1,000 개의 환자 정보

평가 데이터:2,675개의 환자 정보

31개 속성에 대한 설명

나이 - 환자의 나이 (int)

성별 - 성별 환자 식별 (str)

on_thyroxine - 환자가 티록신을 사용하고 있는지 여부 (bool)

티록신에 대한 쿼리 - *환자가 티록신을 복용하고 있는지 여부 (bool)

항갑상선 약 복용 - 환자가 항갑상선 약을 복용하고 있는지 여부 (bool)

sick - 환자가 아픈지 여부 (bool)

임신 - 환자가 임신했는지 여부 (bool)

갑상선_수술 - 환자가 갑상선 수술을 받았는지 여부 (bool)

I131_treatment - 환자가 I131 치료를 받고 있는지 여부 (bool)

query_hypothyroid - 환자가 갑상선 기능 저하증이 있다고 믿는지 여부 (bool)

query_hyperthyroid - 환자가 자신에게 갑상선 기능항진증이 있다고 믿는지 여부 (bool)

리튬 - 환자 여부 * 리튬 (bool)

goitre - 환자에게 갑상선종이 있는지 여부 (bool)

종양 - 환자에게 종양이 있는지 여부 (bool)

뇌하수체하수체 - 환자 여부 * 뇌하수체상수체 (float)

정신 - 환자 여부 * 정신 (bool)

TSH_measured - TSH가 혈액에서 측정되었는지 여부 (bool)

TSH - 실험실 작업에서 나온 혈액 내 TSH 수준 (float)

T3_measured - T3가 혈액에서 측정되었는지 여부 (bool)

T3 - 실험실 작업으로 인한 혈액 내 T3 수준 (float)

TT4_measured - TT4가 혈액에서 측정되었는지 여부 (bool)

TT4 - 실험실 작업으로 인한 혈액 내 TT4 수준 (float)

T4U_measured - T4U가 혈액에서 측정되었는지 여부 (bool)

T4U - 실험실 작업으로 인한 혈액 내 T4U 수준 (float)

FTI_measured - FTI가 혈액에서 측정되었는지 여부 (bool)

FTI - 실험실 작업으로 인한 혈액 내 FTI 수준 (float)

TBG_measured - TBG가 혈액에서 측정되었는지 여부 (bool)

TBG - 실험실 작업에서 나온 혈액 내 TBG 수준 (부동)


추천_소스 - (str)

target - 갑상선항진증 의료 진단 (str)

Patient_id - 환자의 고유 ID (str)

Features(x)

심플한 모형 구성을 위해 4개의 속성만 사용함

나이 - 환자의 나이 (int)

sick - 환자가 아픈지 여부 (bool)

TSH - 실험실 작업에서 나온 혈액 내 TSH 수준 (float)

TT4 - 실험실 작업으로 인한 혈액 내 TT4 수준 (float)

Target(y)

'-' 상태 없음, 'hyperthyroid' (갑상선항진증 상태), 'hypothyroid' (갑상선 기능 저하증), 3가지 형태로 분류를 진행함

진단은 진단된 상태를 나타내는 일련의 문자로 구성되어 있음

진단 '-'은 설명이 필요한 상태가 없음을 나타냄

진단 "X|Y" 형식은 "X와 일치하지만 Y일 가능성이 더 높다"로 해석됨

Letter Diagnosis

hyperthyroid conditions: (갑상선항진증 상태)

A hyperthyroid B T3 toxic C toxic goitre D secondary toxic

hypothyroid conditions: (갑상선 기능 저하증)

E hypothyroid F primary hypothyroid G compensated hypothyroid H secondary hypothyroid

binding protein:

I increased binding protein J decreased binding protein

general health:

K concurrent non-thyroidal illness

replacement therapy: (대체 요법)

L consistent with replacement therapy M underreplaced N overreplaced

antithyroid treatment: (항갑상선 치료)

O antithyroid drugs P I131 treatment Q surgery

miscellaneous: (여러 가지 잡다한)

R discordant assay results S elevated TBG T elevated thyroid hormones

