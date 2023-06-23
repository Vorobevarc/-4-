using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace WindowsFormsApp2
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            textBox4.Text = "13";
            textBox5.Text = "3";
            textBox9.Text = "";
            textBox10.Text = "23";
        }
        private void button3_Click(object sender, EventArgs e)
        {
            int p = int.Parse(textBox4.Text);
            int q = int.Parse(textBox5.Text);
            int n = Math.Abs(p * q);
            textBox8.Text += Environment.NewLine + n.ToString();
            int P = int.Parse(textBox10.Text);
            int fi = Math.Abs((p - 1) * (q - 1));
            textBox7.Text += Environment.NewLine + fi.ToString();
            int E = int.Parse(textBox9.Text);
            int sch = 0;
            int sch1 = 0;
            if (E > 1)
            {
                for (int i = 2; i <= E; i++)
                {
                    if (E % i == 0 && E / i != 1)
                        sch1 += 1;
                    else
                        sch += 1;
                }
                if (sch == E - 1)
                    MessageBox.Show("простое");
                if (sch1 > 0)
                    MessageBox.Show("составное");
            }
            else
                MessageBox.Show(" не простое");
            if (E > fi)
            {
                MessageBox.Show("не подходит");
            }
            if (fi % E == 0)
            {
                MessageBox.Show("не подходит");
            }
            if (E > 1)
            {
                if (E < fi)
                {
                    if (fi % E != 0)
                    {
                        textBox6.Text += Environment.NewLine + "(" + E.ToString() + ", " + n.ToString() + ")";
                        double Ek = Math.Pow(P, E) % n;
                        textBox13.Text += Environment.NewLine + "Шифр: " + Ek.ToString();
                    }
                    else
                        MessageBox.Show("e не подходит");
                }

            }
        }
        private void button4_Click(object sender, EventArgs e)
        {
            int p = int.Parse(textBox4.Text);
            int q = int.Parse(textBox5.Text);
            int n = Math.Abs(p * q);
            int fi = Math.Abs((p - 1) * (q - 1));
            int E = int.Parse(textBox9.Text);
            int P = int.Parse(textBox10.Text);
            double Ek = Math.Pow(P, E) % n;
            int d = int.Parse(textBox11.Text);
            if ((d * E) % fi == 1)
            {
                textBox12.Text += Environment.NewLine + "(" + d.ToString() + ", " + n.ToString() + ")";
                double Pr = Math.Pow(Ek, d) % n;
                textBox14.Text += Environment.NewLine + "Объём: " + Pr.ToString();
            }
            else
                MessageBox.Show(" d не подходит");
        }

        private void button1_Click(object sender, EventArgs e)
        {
            MessageBox.Show("(d * E) % fi = 1");
        }
    }
}
