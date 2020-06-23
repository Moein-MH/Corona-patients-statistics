import requests
from bs4 import BeautifulSoup
from name_ls import ls,up,lw


class covid:
        w_url = 'https://www.worldometers.info/coronavirus/'
        response_w = requests.get(w_url)
        soup_w = BeautifulSoup(response_w.text, 'html.parser')
        data_w = (soup_w.find_all('div', class_="maincounter-number"))
        print("World :")
        print("\nTotal Cases:", data_w[0].text.strip())
        print("Total Deaths:", data_w[1].text.strip())
        print("Total Recovered:", data_w[2].text.strip())
        print("-------")

def country_meter(url):
	response_c = requests.get(url)
	soup_c = BeautifulSoup(response_c.text, 'html.parser')
	data_c = soup_c.find_all('div', class_="maincounter-number")
	print("\n>>>\n")
	print("---Total Cases:", data_c[0].text.strip())
	print("---Total Deaths:", data_c[1].text.strip())
	print("---Total Recovered:", data_c[2].text.strip())
	print("----------------------"+("-"*len(data_c[2].text.strip())))


def country():
        contry_put = input("\nPlease Enter Contry name: ")
        if contry_put in ls:
                c_url = f'https://www.worldometers.info/coronavirus/{ls[contry_put]}'
                country_meter(c_url)

        elif contry_put in up:
                c_url = f'https://www.worldometers.info/coronavirus/{up[contry_put]}'
                country_meter(c_url)

        elif contry_put in lw:
                c_url = f'https://www.worldometers.info/coronavirus/{lw[contry_put]}'
                country_meter(c_url)
        elif contry_put == "exit":
                exit()
        
        else:
                print("\nThis country is not on the list !\n")
                
country()
while True:
        
        q_put = input("\nContinue? (yes/no) : ")

        if q_put == "yes": country()
        elif q_put == "no": exit()
        
