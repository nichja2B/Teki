//
//  ViewController.swift
//  Telki
//
//  Created by Laurent Lafarge on 13/09/2018.
//  Copyright © 2018 Laurent Lafarge. All rights reserved.
//

import UIKit

class ViewController: UIViewController {

// (var celebrities et activities) declaration de la variable dans un tableau
    var celebrities = ["Le Steeve Jobs", "Le Zinedine Zidane", "La Madonna", "Le Karl Lagarfield", "La Scarlett Johanson"]
    var activities = ["de la raclette", "du dance floor", "du barbecue", "de la surprise ratée", "des blagues lourdes"]


    @IBOutlet weak var QuoteLabel: UILabel!


    @IBAction func changeQuote() {
        // declaration de la variable qui nous donne un index aléatoire du tableau puis créationde la variable celebrity qui appel de la variable pour recuperer le nom de l'index puis la fonction print pour ecrire le nom de l'index du tableau
        let randomIndex1 = Int(arc4random_uniform(UInt32(celebrities.count)))
        let celebrity = celebrities[randomIndex1]


         let randomIndex2 = Int(arc4random_uniform(UInt32(activities.count)))
        let activity = activities[randomIndex2]

        let quote = "Tu es " + celebrity + " " + activity + " !"
        QuoteLabel.text = quote

    }

}
