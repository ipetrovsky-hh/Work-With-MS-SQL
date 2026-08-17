CREATE TABLE dbo.EMPLOYEE (
  Id INTEGER PRIMARY KEY,
  Code nvarchar(50) NOT NULL,
  Name nvarchar(50) NOT NULL,
  StatusId nvarchar(50) NOT NULL
);

-- insert
INSERT INTO dbo.EMPLOYEE(Id,Code,Name,StatusId) 
VALUES(1,'SBR003-202001',N'Конкурс СМСП','45');

INSERT INTO dbo.EMPLOYEE(Id,Code,Name,StatusId) 
VALUES(2,'SBR003-202002',N'Запрос предложений','2');

SELECT Id, Code, Name, StatusId FROM EMPLOYEE FOR XML path('row'), ROOT('data')
