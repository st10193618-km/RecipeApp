# RecipeApp
using System;
using System.Collections.Generic;

class RecipeApp
{
    static void Main()
    {
        Console.WriteLine("Welcome to the Recipe Application!");
        
        // Get the number of ingredients
        Console.Write("Enter the number of ingredients: ");
        int numIngredients = int.Parse(Console.ReadLine());
        
        List<string> ingredients = new List<string>();
        
        for (int i = 0; i < numIngredients; i++)
        {
            Console.Write($"Enter ingredient {i + 1} (name, quantity, unit): ");
            string ingredient = Console.ReadLine();
            ingredients.Add(ingredient);
        }
        
        // Get the number of steps
        Console.Write("Enter the number of steps: ");
        int numSteps = int.Parse(Console.ReadLine());
        
        List<string> steps = new List<string>();
        
        for (int i = 0; i < numSteps; i++)
        {
            Console.Write($"Enter step {i + 1} description: ");
            string step = Console.ReadLine();
            steps.Add(step);
        }
        
        // Display the recipe
        Console.WriteLine("\nRecipe Summary:");
        Console.WriteLine("Ingredients:");
        foreach (var ingredient in ingredients)
        {
            Console.WriteLine("- " + ingredient);
        }
        
        Console.WriteLine("\nSteps:");
        for (int i = 0; i < steps.Count; i++)
        {
            Console.WriteLine($"{i + 1}. {steps[i]}");
        }
    }
}
