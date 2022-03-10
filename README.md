package segundopuntoparcial;

import javax.swing.JOptionPane;

public class Segundopuntoparcial {

    public static void main(String[] args) {
        String nombre = JOptionPane.showInputDialog("Ingrese su nombre por favor: ");
        String codigo = JOptionPane.showInputDialog("digite su codigo por favor");

        try {

            double nota1 = Double.parseDouble(JOptionPane.showInputDialog("Ingrese la nota de su primer corte"));
            double nota2 = Double.parseDouble(JOptionPane.showInputDialog("Ingrese la nota de su segundo corte"));
            double nota3 = Double.parseDouble(JOptionPane.showInputDialog("Ingrese la nota de su tercer corte"));

            double calculoCorte1 = (30 * nota1 / 100);
            double calculoCorte2 = (25 * nota2 / 100);
            double calculoCorte3 = (45 * nota3 / 100);

            double calculoNotaFinal = calculoCorte1 + calculoCorte2 + calculoCorte3;

            JOptionPane.showMessageDialog(null, "El estudiante con nombre: " + nombre + "\n codigo: " + codigo
                    + "\n Nota Final: " + calculoNotaFinal);

        } catch (NumberFormatException ex) {
            JOptionPane.showMessageDialog(null, "Solo puede ingresar numeros");
        }

    }

}
