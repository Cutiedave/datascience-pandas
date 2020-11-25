# datascience-pandas
def proportion_of_education():
    import pandas as pd
    nu=pd.read_csv('assets/NISPUF17.csv')
    a=len(nu['EDUC1'][nu['EDUC1']==1])
    b=len(nu['EDUC1'][nu['EDUC1']==2])
    c=len(nu['EDUC1'][nu['EDUC1']==3])
    d=len(nu['EDUC1'][nu['EDUC1']==4])
    e=a+b+c+d
    proportion_of_education={}
    proportion_of_education["less than high school"]=a/e
    proportion_of_education["high school"]=b/e
    proportion_of_education["more than high school but not college"]=c/e
    proportion_of_education["college"]=d/e
    return proportion_of_education

proportion_of_education()
