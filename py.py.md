def get_cidr_notation(ip_class):
    if ip_class == "A":
        return "/8"
    elif ip_class == "B":
        return "/16"
    elif ip_class == "C":
        return "/24"
    else:
        return "Invalid IP class Use A, B, or C."

if name == "main":
    ip_address = input("Enter the IP address: ")
    ip_class = input("Enter the IP class (A, B, or C): ")

    cidr_notation = get_cidr_notation(ip_class)
    print(f"CIDR notation: {cidr_notation}"