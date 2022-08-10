# nutritionalscore

package main

import (
	"fmt"
)

//ini adalah data yang ingin dimasukan kedalam score, yang mana setelah di jalankan akan muncul score akhir dari file lain
func main() {

	ns := GetNutritionalScore(NutritionalData{
		Energy:              EnergyFromKcal(100),
		Sugars:              SugarGram(10),
		SaturatedFattyAcids: SaturatedFattyAcids(2),
		Sodium:              SodiumMiligram(500),
		Fruits:              FruitsPercent(60),
		Fibre:               FibreGram(4),
		Protein:             ProteinGram(2),
	}, Food)

	fmt.Printf("Nutritional Score:%d\n", ns.Value)
	fmt.Printf("NutriScore: %s\n", ns.GetNutritionalScore())
}
