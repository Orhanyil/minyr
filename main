package main

import (
	"bufio"
	"fmt"
	"os"

	"github.com/Orhanyil/minyr/yr"
)

func main() {
	var input string
	scanner := bufio.NewScanner(os.Stdin)

	for {
		fmt.Println("Venligst velg convert, average eller exit:")

		if !scanner.Scan() {
			break
		}
		input = scanner.Text()

		switch input {
		case "q", "exit":
			fmt.Println("exit")
			return

		case "convert":
			fmt.Println("Konverterer alle målingene gitt i grader Celsius til grader Fahrenheit...")
			// 'convert' for å gjennomføre konverteringen
			yr.ConvertTemperature()

		case "average":
			fmt.Println("Gjennomsnitt-kalkulator")

			for {
				// 'average' for å få skrevet ut gjennomsnittstemperatur for hele perioden av
				// temperaturmålinger.
				yr.AverageTemperature()

				var input2 string
				scanjn := bufio.NewScanner(os.Stdin)
				fmt.Println("Tilbake til hovedmeny? (j/n)")
				for scanjn.Scan() {
					input2 = scanjn.Text()
					if input2 == "j" {
						break
					} else if input2 == "n" {
						break
					}
				}
				if input2 == "j" {
					break
				}
			}
		}
	}
	fmt.Println("Avslutter program.")
}
