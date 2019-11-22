# Lab_13
#OOP
class delivery_personnel:
	def __init__(self, name, years_of_service, company,is_drone, zip_codes_covered):
		self.name = name
		self.years_of_service = years_of_service
		self.company = company
		self.is_drone = is_drone
		self.zip_codes_covered = zip_codes_covered


	#getters
	def get_years_of_service(self):
		return(self.years_of_service)

	def get_company(self):
		return(self.company)

	def get_zip_codes_covered(self):
		return(self.zip_codes_covered)

	#setters
	def set_years_of_service(self, d):
		self.years_of_service = d

	def set_company(self, d):
		self.company = d 

	def set_zip_codes_covered(self, d):
		self.zip_codes_covered = d 


	def deliver(self, input_list):

		delivered_already = [i for i in input_list if i in self.zip_codes_covered]
		print(delivered_already)
		

def main():
	zip_list = [20854, 35285, 20173, 26836]
	person_1 = delivery_personnel(name = "Mike", years_of_service = 14, company = "Fedex", is_drone = True, zip_codes_covered = [20854, 25383, 68369])

	person_1.deliver(zip_list)

if __name__ == "__main__":
	main()
