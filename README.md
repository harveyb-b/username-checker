# username-checker
checks to see if username exists in sqldatabase

           SqlDataAdapter da = new SqlDataAdapter("Select Username From createAccount where Username = '" + txtUsername.Text + "'", con);
            DataTable dt = new DataTable();
            da.Fill(dt);
            if (dt.Rows.Count >= 1)
            {
                MessageBox.Show("Username already exists!");
                txtUsername.Text = "";
            }
            else
