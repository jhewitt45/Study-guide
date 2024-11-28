#include <iostream>
#include <vector>
#include <string>

struct Section {
    std::string topic;
    std::vector<std::string> questions;
};

void displayStudyGuide(const std::vector<Section>& studyGuide) {
    for (const auto& section : studyGuide) {
        std::cout << "### " << section.topic << " ###" << std::endl;
        for (size_t i = 0; i < section.questions.size(); ++i) {
            std::cout << i + 1 << ". " << section.questions[i] << std::endl;
        }
        std::cout << std::endl;
    }
}

int main() {
    std::vector<Section> studyGuide = {
        {
            "Integration Techniques",
            {
                "Evaluate ∫ (3x^2 + 2x + 1) dx.",
                "Solve ∫ sin(x)/cos^2(x) dx.",
                "Use u-substitution to evaluate ∫ x√(x^2 + 1) dx.",
                "Compute ∫ x e^x dx using integration by parts.",
                "Find ∫ sin^3(x)cos(x) dx.",
                "Evaluate ∫ dx/√(9 - x^2) using trigonometric substitution.",
                "Solve ∫ (5x - 2)/(x^2 - 4x + 3) dx using partial fraction decomposition.",
                "Determine whether ∫₁^∞ 1/x^2 dx converges or diverges.",
                "Compute ∫ dx/(x^2 + 1).",
                "Evaluate ∫ 1/(x ln(x)) dx using substitution.",
                "Solve ∫ ln(x) dx using integration by parts.",
                "Find the integral ∫ sec^2(x) dx."
            }
        },
        {
            "Applications of Integration",
            {
                "Find the area between y = x^2 and y = 2x from x = 0 to x = 2.",
                "Compute the volume of the solid formed by revolving y = x^2 about the x-axis for x ∈ [0, 2] using the disk method.",
                "Use the washer method to find the volume of the region between y = √x and y = x, revolved about the y-axis.",
                "Find the volume of the solid obtained by rotating y = 1/x, x ∈ [1, 2], about the y-axis using the shell method.",
                "Calculate the arc length of y = ln(x) from x = 1 to x = e.",
                "Determine the surface area of the solid formed by rotating y = √x about the x-axis, for x ∈ [1, 4].",
                "Solve a work problem: Find the work done in pumping water from a tank with a hemispherical bottom of radius 5 m, filled to a depth of 3 m.",
                "Calculate the pressure at the base of a vertical plate submerged in a fluid of density ρ when the plate is described by y = 4 - x^2.",
                "Compute W = ∫₀² (3x^2 - 4x) dx to find the work done by a variable force.",
                "Solve for the total force acting on a vertical dam shaped like y = √x, submerged in water up to x = 4."
            }
        },
        {
            "Sequences and Series",
            {
                "Determine whether the sequence aₙ = n/(n^2 + 1) converges or diverges.",
                "Test the series ∑₁^∞ 1/n^2 for convergence.",
                "Is ∑₁^∞ (-1)^n (1/n) convergent? Justify using the Alternating Series Test.",
                "Apply the Ratio Test to ∑₁^∞ n!/2^n.",
                "Use the Root Test to determine whether ∑₁^∞ (2^n/n!) converges.",
                "Find the radius of convergence for ∑₀^∞ x^n/n!.",
                "Write the first four terms of the Taylor series for f(x) = e^x centered at x = 0.",
                "Approximate e^(0.1) using the first three terms of its Maclaurin series.",
                "Express 1/(1 - x) as a power series and state its radius of convergence.",
                "Determine whether ∑₁^∞ ln(n)/n^2 converges using the Comparison Test."
            }
        },
        {
            "Parametric Equations and Polar Coordinates",
            {
                "Find dy/dx for the parametric equations x = t^2, y = t^3.",
                "Compute the arc length of the curve given by x = t^2, y = t^3, for t ∈ [0, 1].",
                "Convert the polar equation r = 2cos(θ) to Cartesian coordinates.",
                "Find the area enclosed by one petal of the polar curve r = sin(3θ).",
                "Compute the arc length of r = 2 + sin(θ) for θ ∈ [0, π].",
                "Determine whether the parametric curve x = t^2, y = t^3 intersects itself.",
                "Use parametric equations to find the tangent line to x = sin(t), y = cos(t) at t = π/4.",
                "Find the area enclosed by r = 1 + cos(θ) for θ ∈ [0, 2π]."
            }
        },
        {
            "Differential Equations",
            {
                "Solve dy/dx = 3x^2, with initial condition y(0) = 2.",
                "Solve dy/dx + y = e^x using the integrating factor method.",
                "Determine the general solution of dy/dx = ky.",
                "Solve dy/dx = -2xy using the method of separable equations.",
                "A population grows at a rate proportional to its size. If P(0) = 100 and P(2) = 200, find P(t).",
                "Solve the differential equation dP/dt = 0.1P(100 - P).",
                "Use Euler’s method to approximate y(1) for dy/dx = y - x^2 with y(0) = 1, step size h = 0.5.",
                "Solve the cooling problem dT/dt = -k(T - 20) with T(0) = 80.",
                "Determine the equilibrium solution for dy/dx = y(1 - y).",
                "A tank contains 100 L of water with 10 g of salt dissolved. Water containing 1 g/L of salt flows in at 5 L/min, while the solution flows out at the same rate. Find the salt concentration at t = 10 minutes."
            }
        }
    };

    displayStudyGuide(studyGuide);

    return 0;
}
