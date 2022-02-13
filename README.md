# Comment-App
We have used SQL Server Database. Please use the same SQL Server database. Database name should be FeedBack.
Please use the below SQL Queries to create the required database tables.
USE [FeedBack]
GO


SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[UserDetails](
	[LoginID] [int] IDENTITY(1,1) NOT NULL,
	[Email] [nvarchar](200) NULL,
	[Password] [nvarchar](200) NULL,
	[SecretCode] [nvarchar](200) NULL,
	[Active] [bit] NULL,
	[InsertedBy] [nvarchar](200) NULL,
	[InsertedOn] [datetime] NULL,
	[UpdatedBy] [nvarchar](200) NULL,
	[UpdatedOn] [datetime] NULL,
PRIMARY KEY CLUSTERED 
(
	[LoginID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO



USE [FeedBack]
GO

SET ANSI_NULLS ON
GO

SET QUOTED_IDENTIFIER ON
GO

CREATE TABLE [dbo].[CommentsDetails](
	[CmtID] [int] IDENTITY(1,1) NOT NULL,
	[Email] [nvarchar](200) NULL,
	[Comments] [nvarchar](2000) NULL,
	[Active] [bit] NULL,
	[InsertedBy] [nvarchar](200) NULL,
	[InsertedOn] [datetime] NULL,
	[UpdatedBy] [nvarchar](200) NULL,
	[UpdatedOn] [datetime] NULL,
PRIMARY KEY CLUSTERED 
(
	[CmtID] ASC
)WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON, OPTIMIZE_FOR_SEQUENTIAL_KEY = OFF) ON [PRIMARY]
) ON [PRIMARY]
GO


Change the connection string in the web configuration file according to the created database.
After the above steps, you can run the application directly and validate the test cases.
