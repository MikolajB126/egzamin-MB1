Window x:Class="AplikacjaPracownicza.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        Title="Aplikacja Pracownicza"
        Height="500" Width="800">

    <Grid Margin="10">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="*"/>
        </Grid.RowDefinitions>

        <StackPanel Orientation="Horizontal" Margin="0,0,0,10" VerticalAlignment="Top">
            <StackPanel Margin="5">
                <Label Content="Login"/>
                <TextBox x:Name="LoginBox" Width="120"/>
            </StackPanel>
            <StackPanel Margin="5">
                <Label Content="Email"/>
                <TextBox x:Name="EmailBox" Width="200"/>
            </StackPanel>
            <StackPanel Margin="5">
                <Label Content="Hasło"/>
                <PasswordBox x:Name="PasswordBox" Width="120"/>
            </StackPanel>
            <Button Content="Zaloguj" Width="80" Margin="5" VerticalAlignment="Bottom" Click="Login_Click"/>
        </StackPanel>

        <StackPanel Grid.Row="1">
            <StackPanel Orientation="Horizontal" Margin="0,0,0,10">
                <Label Content="Od:" VerticalAlignment="Center"/>
                <DatePicker x:Name="FromDate" Width="150" Margin="5"/>
                <Label Content="Do:" VerticalAlignment="Center"/>
                <DatePicker x:Name="ToDate" Width="150" Margin="5"/>
                <Button Content="Filtruj" Width="80" Margin="5" Click="Filter_Click"/>
            </StackPanel>

            <DataGrid x:Name="TasksGrid" AutoGenerateColumns="True" Height="350"/>
        </StackPanel>
    </Grid>
/Window>
