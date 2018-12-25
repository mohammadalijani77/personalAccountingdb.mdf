# personalAccountingdb.mdf
CREATE PROCEDURE [dbo].[PDeletAshkhas]
	@Id int 


	as 
begin 
set nocount on 



delete from tbl_Ashkhas where Id=@Id

end



CREATE PROCEDURE [dbo].[PInsertDaryaft]
	@mablagh int,
	@group1 nvarchar(50),
	@hesab nvarchar(50),
	@shakhs nvarchar(50),
	@data nvarchar(50),
	@description nvarchar(max)

AS
begin 
set nocount on 

insert into tbl_Daryaft values (@mablagh,@group1 ,@hesab,@shakhs,@data,@description)




end



CREATE PROCEDURE [dbo].[PUpdaeAshkhas]
	@Id int,
	@name nvarchar(50),
	@description nvarchar(max),
	@flig tinyint,
	@data nvarchar(50) 
AS
	begin 


	update tbl_Ashkhas set name=@name ,description=@description,flig=@flig,data=@data
	where Id=@Id


	end
