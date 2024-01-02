# QueryDocument
given total explanation on find query, finding  query using condition, specify  and condition
Where we are using find query we seen all the inserted documents
 demodb> db.employes.find()
[
  {
    _id: ObjectId('657af5bb3289944f06de24f4'),
    EMPLOYEE_ID: '1',
    FIRST_NAME: 'Renu',
    SECOND_NAME: 'Pac',
    EMAIL: 'renu123@gmail.com',
    PHONE_NUMBER: '91829345',
    HIRE_DATE: '26-oct-05',
    JOB_ID: 'ST_CLEARK',
    MANGER_ID: '123',
    DEPARTEMENT_ID: '50',
    Salary: '18000'
  },
  {
    _id: ObjectId('657af70d3289944f06de24f5'),
    EMPLOYEE_ID: '2',
    FIRST_NAME: 'Renuka',
    SECOND_NAME: 'Pachava',
    EMAIL: 'renu321@gmail.com',
    PHONE_NUMBER: '918367838',
    HIRE_DATE: '28-oct-08',
    JOB_ID: 'SL_CLEARK',
    MANGER_ID: '321',
    DEPARTEMENT_ID: '60',
    Salary: '15000\n'
  },
  {
    _id: ObjectId('657af7883289944f06de24f6'),
    EMPLOYEE_ID: '3',
    FIRST_NAME: 'naga',
    SECOND_NAME: 'lakshmi',
    EMAIL: 'naga123@gmail.com',
    PHONE_NUMBER: '94374646369837',
    HIRE_DATE: '26-oct-05',
    JOB_ID: 'ST_CLEARK',
    MANGER_ID: '132',
    DEPARTEMENT_ID: '50',
    Salary: '45000'
  },
  {
    _id: ObjectId('657af7d93289944f06de24f7'),
    EMPLOYEE_ID: '4',
    FIRST_NAME: 'Ravanamma',
    SECOND_NAME: 'Lakshmi',
    EMAIL: 'rava123@gmail.com',
    PHONE_NUMBER: '94848346392889',
    HIRE_DATE: '28-oct-08',
    JOB_ID: 'SL_CLEARK',
    MANGER_ID: '143',
    DEPARTEMENT_ID: '60',
    Salary: '54000'
  },
  {
    _id: ObjectId('657af83a3289944f06de24f8'),
    EMPLOYEE_ID: '5',
    FIRST_NAME: 'Vengamma',
    SECOND_NAME: 'Bolla',
    EMAIL: 'vengi123@gmail.com',
    PHONE_NUMBER: '96848465784',
    HIRE_DATE: '25-oct-07',
    JOB_ID: 'PR_CLEARK',
    MANGER_ID: '678',
    DEPARTEMENT_ID: '100',
    Salary: '23000'
  },
  {
    _id: ObjectId('657b00493289944f06de24f9'),
    EMPLOYEE_ID: '6',
    FIRST_NAME: 'Nagamani',
    SECOND_NAME: 'Talu',
    EMAIL: 'mani123@gmail.com',
    PHONE_NUMBER: '968487865',
    HIRE_DATE: '25-oct-07',
    JOB_ID: 'PR_CLEARK',
    MANGER_ID: '678',
    DEPARTEMENT_ID: '100',
    Salary: '32000'
  },
  {
    _id: ObjectId('657b01e03289944f06de24fa'),
    EMPLOYEE_ID: '7',
    FIRST_NAME: 'Veekshu',
    SECOND_NAME: 'pachl',
    EMAIL: 'veeks123@gmail.com',
    PHONE_NUMBER: '968938534',
    HIRE_DATE: '13-Nov-09',
    JOB_ID: 'MR_Mang',
    MANGER_ID: '876',
    DEPARTEMENT_ID: '78',
    Salary: '50000'
  },
  {
    _id: ObjectId('657b02173289944f06de24fb'),
    EMPLOYEE_ID: '8',
    FIRST_NAME: 'Charan',
    SECOND_NAME: 'velar',
    EMAIL: 'char123@gmail.com',
    PHONE_NUMBER: '9689398443',
    HIRE_DATE: '25-Jan-09',
    JOB_ID: 'MR_Mang',
    MANGER_ID: '455',
    DEPARTEMENT_ID: '45',
    Salary: '15000'
  },
  {
    _id: ObjectId('657b02593289944f06de24fc'),
    EMPLOYEE_ID: '9',
    FIRST_NAME: 'Revanth',
    SECOND_NAME: 'Taluch',
    EMAIL: 'reva123@gmail.com',
    PHONE_NUMBER: '9689398443',
    HIRE_DATE: '25-Dec-09',
    JOB_ID: 'MR_CLEARK',
    MANGER_ID: '756',
    DEPARTEMENT_ID: '10',
    Salary: '74000'
  },
  {
    _id: ObjectId('657b02bb3289944f06de24fd'),
    EMPLOYEE_ID: '10',
    FIRST_NAME: 'Nani',
    SECOND_NAME: 'Bhasv',
    EMAIL: 'nani123@gmail.com',
    PHONE_NUMBER: '968234567',
    HIRE_DATE: '23-Feb-15',
    JOB_ID: 'MR_Time',
    MANGER_ID: '545',
    DEPARTEMENT_ID: '67',
    Salary: '23000'
  },
  {
    _id: ObjectId('65902a216189e4ff829cab36'),
    EMPLOYEE_ID: '11',
    FIRST_NAME: 'Chinna',
    SECOND_NAME: 'Talu',
    EMAIL: 'chinna@gmail.com',
    PHONE_NUMBER: '63638226',
    Salary: '2300'
  }


# In the above documents we  finding the specify equality condition



demodb> db.employes.find({Salary : '2300'});
[
  {
    _id: ObjectId('65902a216189e4ff829cab36'),
    EMPLOYEE_ID: '11',
    FIRST_NAME: 'Chinna',
    SECOND_NAME: 'Talu',
    EMAIL: 'chinna@gmail.com',
    PHONE_NUMBER: '63638226',
    Salary: '2300'
  }
]
# In the above documents we  finding the specify equality condition

demodb> db.employes.find({PHONE_NUMBER : '63638226'});
[
  {
    _id: ObjectId('65902a216189e4ff829cab36'),
    EMPLOYEE_ID: '11',
    FIRST_NAME: 'Chinna',
    SECOND_NAME: 'Talu',
    EMAIL: 'chinna@gmail.com',
    PHONE_NUMBER: '63638226',
    Salary: '2300'
  }
]
# In the above documents we  finding the specify equality condition

demodb> db.employes.find({FIRST_NAME : 'Nani'});
[
  {
    _id: ObjectId('657b02bb3289944f06de24fd'),
    EMPLOYEE_ID: '10',
    FIRST_NAME: 'Nani',
    SECOND_NAME: 'Bhasv',
    EMAIL: 'nani123@gmail.com',
    PHONE_NUMBER: '968234567',
    HIRE_DATE: '23-Feb-15',
    JOB_ID: 'MR_Time',
    MANGER_ID: '545',
    DEPARTEMENT_ID: '67',
    Salary: '23000'
  }
]
# Finding specify condition
demodb> db.employes.find({Salary :{$in: ['2300','18000','45000','54000']} });
[
  {
    _id: ObjectId('657af5bb3289944f06de24f4'),
    EMPLOYEE_ID: '1',
    FIRST_NAME: 'Renu',
    SECOND_NAME: 'Pac',
    EMAIL: 'renu123@gmail.com',
    PHONE_NUMBER: '91829345',
    HIRE_DATE: '26-oct-05',
    JOB_ID: 'ST_CLEARK',
    MANGER_ID: '123',
    DEPARTEMENT_ID: '50',
    Salary: '18000'
  },
  {
    _id: ObjectId('65902a216189e4ff829cab36'),
    EMPLOYEE_ID: '11',
    FIRST_NAME: 'Chinna',
    SECOND_NAME: 'Talu',
    EMAIL: 'chinna@gmail.com',
    PHONE_NUMBER: '63638226',
    Salary: '2300'
  },
  {
    _id: ObjectId('657af7883289944f06de24f6'),
    EMPLOYEE_ID: '3',
    FIRST_NAME: 'naga',
    SECOND_NAME: 'lakshmi',
    EMAIL: 'naga123@gmail.com',
    PHONE_NUMBER: '94374646369837',
    HIRE_DATE: '26-oct-05',
    JOB_ID: 'ST_CLEARK',
    MANGER_ID: '132',
    DEPARTEMENT_ID: '50',
    Salary: '45000'
  },
  {
    _id: ObjectId('657af7d93289944f06de24f7'),
    EMPLOYEE_ID: '4',
    FIRST_NAME: 'Ravanamma',
    SECOND_NAME: 'Lakshmi',
    EMAIL: 'rava123@gmail.com',
    PHONE_NUMBER: '94848346392889',
    HIRE_DATE: '28-oct-08',
    JOB_ID: 'SL_CLEARK',
    MANGER_ID: '143',
    DEPARTEMENT_ID: '60',
    Salary: '54000'
  }
]

 
# Specify AND condition
demodb> db.employes.find({$and : [{Salary : '15000'},{FIRST_NAME: 'Charan'}] });
[
  {
    _id: ObjectId('657b02173289944f06de24fb'),
    EMPLOYEE_ID: '8',
    FIRST_NAME: 'Charan',
    SECOND_NAME: 'velar',
    EMAIL: 'char123@gmail.com',
    PHONE_NUMBER: '9689398443',
    HIRE_DATE: '25-Jan-09',
    JOB_ID: 'MR_Mang',
    MANGER_ID: '455',
    DEPARTEMENT_ID: '45',
    Salary: '15000'
  }
]
